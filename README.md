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

-Sobel<br>
-Laplacian<br>
-Canny
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
```
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
```
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
```
laplacian=cv2.Laplacian(img,cv2.CV_64F)
plt.figure(1)
plt.imshow(laplacian,cmap='gray')
plt.title('Laplacian'),plt.xticks([]),plt.yticks([])
plt.show()

```
### CANNY EDGE DETECTOR:
```
canny_edges=cv2.Canny(img,120,150)
plt.figure(1)
plt.imshow(canny_edges,cmap='gray')
plt.title('Canny Edges'),plt.xticks([]),plt.yticks([])
plt.show()
```


## Output:
### SOBEL EDGE DETECTOR:

<br>
![eren1](https://user-images.githubusercontent.com/93860256/231750192-0e6f1de3-93ba-4fb6-a54f-40473bb4bcf5.png)
![eren2](https://user-images.githubusercontent.com/93860256/231750196-ad8539fd-b999-4994-a351-c8a2c041b70d.png)
![eren3](https://user-images.githubusercontent.com/93860256/231750200-a8b3fad3-0998-4f13-b9aa-28aa5c227128.png)
![eren4](https://user-images.githubusercontent.com/93860256/231750203-4b5d5f10-8b0a-4f92-8333-46ecc2f6ba03.png)
<br>



### LAPLACIAN EDGE DETECTOR:

<br>

![eren5](https://user-images.githubusercontent.com/93860256/231750204-1d05a4a1-3eb5-4a58-b99d-8813cff9c32f.png)
<br>



### CANNY EDGE DETECTOR:

<br>

![eren6](https://user-images.githubusercontent.com/93860256/231750212-02de5edb-f1c4-4dd9-ada7-4bad44438bae.png)
<br>


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
