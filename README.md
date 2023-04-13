# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules

### Step2:
Perform the edge detection on the image

(i) Sobel<br>
(ii) Laplacian<br>
(iii) Canny
<br>

### Step3:
Display the original images with the edge detected images
 
## Program:
```
# Developed by: Senthil Kumar S
# Reg No: 212221230091
```
### Import the packages:
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt 
```
### Load the image, Convert to grayscale and remove noise:
```python
pic=cv2.imread('er1.jpg')
cv2.imshow('Original',pic)

togray = cv2.cvtColor(pic,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR To HSV',togray)

img=cv2.GaussianBlur(togray,(3,3),0)
cv2.imshow('Gaussian Blur',img)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### SOBEL EDGE DETECTOR:
```python
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.imshow(img,cmap='gray')
plt.title('Original'),plt.xticks([]),plt.yticks([])
plt.show()
plt.figure(1)
plt.imshow(sobelx,cmap='gray')
plt.title('Sobelx'),plt.xticks([]),plt.yticks([])
plt.show()
plt.figure(1)
plt.imshow(sobely,cmap='gray')
plt.title('Sobely'),plt.xticks([]),plt.yticks([])
plt.show()
plt.figure(1)
plt.imshow(sobelxy,cmap='gray')
plt.title('Sobelxy'),plt.xticks([]),plt.yticks([])
plt.show()
```
### LAPLACIAN EDGE DETECTOR:
```python
laplacian=cv2.Laplacian(img,cv2.CV_64F)
plt.figure(1)
plt.imshow(laplacian,cmap='gray')
plt.title('Laplacian'),plt.xticks([]),plt.yticks([])
plt.show()

```
### CANNY EDGE DETECTOR:
```python
canny_edges=cv2.Canny(img,120,150)
plt.figure(1)
plt.imshow(canny_edges,cmap='gray')
plt.title('Canny Edges'),plt.xticks([]),plt.yticks([])
plt.show()
```


## Output:
### SOBEL EDGE DETECTOR:

![eren1](https://user-images.githubusercontent.com/93860256/231751635-0f937712-c0c5-421b-bf25-2b6436121b4b.jpg)
![eren2](https://user-images.githubusercontent.com/93860256/231751632-4b52e415-6129-4837-9335-be26af56941b.jpg)
![eren3](https://user-images.githubusercontent.com/93860256/231751629-1a8896aa-1eb2-4a1d-95e9-a7c650732ea3.jpg)
![eren4](https://user-images.githubusercontent.com/93860256/231751622-a34c2d69-248f-4bb2-bc5f-24f023f148aa.jpg)


### LAPLACIAN EDGE DETECTOR:

<br>

![eren5](https://user-images.githubusercontent.com/93860256/231751643-5e890b23-c9b4-4ce1-b88e-572354aa5322.jpg)
<br>



### CANNY EDGE DETECTOR:

<br>

![eren6](https://user-images.githubusercontent.com/93860256/231751639-81a3aee1-8f65-409e-b081-fd174ffd32df.jpg)
<br>


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
