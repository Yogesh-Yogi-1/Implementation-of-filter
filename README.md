# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.
</br> 

### Step2
Convert the image from BGR to RGB.
</br> 

### Step3
Apply the required filters for the image separately.
</br> 

### Step4
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
End the program.
</br> 

## Program:
### Developed By  : YOGESH. V
### Register Number: 212223230250
</br>

### 1. Smoothing Filters

#### i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("rome.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```
#### ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
#### iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
#### iv)Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
#### i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
#### ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
</br>

#### i) Using Averaging Filter
![image](https://github.com/user-attachments/assets/6986940b-0375-4e6e-814c-8fda1ffb0e76)

</br>

#### ii)Using Weighted Averaging Filter
![image](https://github.com/user-attachments/assets/58174389-2cb5-45f7-9491-85a2cc41f1e6)

</br>

#### iii)Using Gaussian Filter
![image](https://github.com/user-attachments/assets/1ad661a7-dae6-4aac-98e6-847d7e22fba9)

</br>

#### iv) Using Median Filter
![image](https://github.com/user-attachments/assets/08c2aaa4-beab-4865-b96f-19e87e04154f)

</br>

### 2. Sharpening Filters
</br>

#### i) Using Laplacian Kernal
![image](https://github.com/user-attachments/assets/76e4ab7a-a18e-45ad-b2da-e38bccd4dda1)

</br>

#### ii) Using Laplacian Operator
![image](https://github.com/user-attachments/assets/3c6d6e91-4bb6-4330-b597-35f0dfe98ad2)

</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
