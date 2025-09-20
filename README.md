# Implementation-of-filter
## Name : Yaazhini S
## Register no:212224230308
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import the required libraries.


### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.
## Program:
### Developed By   : yaazhini S
### Register Number:212224230308
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Imgage2.jpg")
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
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
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
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
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
iv)Using Median Filter
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
i) Using Laplacian Linear Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
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

i) Using Averaging Filter
</br>
</br><img width="1033" height="402" alt="image" src="https://github.com/user-attachments/assets/7bfc7f50-1e21-4fe8-aedd-1ea778f380ae" />

</br>
</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br><img width="778" height="307" alt="image" src="https://github.com/user-attachments/assets/91826437-12d5-455a-bc10-c530ba7e6eeb" />

</br>
</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
</br><img width="810" height="317" alt="image" src="https://github.com/user-attachments/assets/733aec6e-00ff-4442-a33c-253a8b993d7c" />

</br>
</br>

iv) Using Median Filter
</br>
</br>
</br><img width="1023" height="387" alt="image" src="https://github.com/user-attachments/assets/2c46e790-1734-4440-9c5a-a04f9ce83fa7" />

</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br><img width="745" height="281" alt="image" src="https://github.com/user-attachments/assets/6baa8d33-00d9-47d9-a86c-345bbf6e6670" />

</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
</br><img width="734" height="275" alt="image" src="https://github.com/user-attachments/assets/d1895256-a0d6-417b-8cf1-442e3c09a65b" />

</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
