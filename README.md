# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM :
### Developed By : SD ABBU REHAN
### Register Number : 212223240165

### Importing packages,load and convert to gray image
```python
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('orangeflower.jpg',0)
gray=cv2.cvtColor(image,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.imshow(gray)
```
### Sobel Edge Detector

### Sobel X  
```python
sobel_x = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobel_x,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### Sobel Y
```python
sobel_y = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobel_y,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### Sobel XY
```python
sobel_xy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobel_xy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### Laplacian Edge Detector
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

### Canny Edge Detector
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## OUTPUT:
### Gray Image
![image](https://github.com/Abburehan/EDGE-DETECTION/assets/138849336/3c9bafcc-2799-42c7-b571-0775407ab11c)

### SOBEL EDGE DETECTOR
### Sobel X
![image](https://github.com/Abburehan/EDGE-DETECTION/assets/138849336/c87595e0-336b-4245-aae8-0eeb2ce25bb0)

### Sobel Y
![image](https://github.com/Abburehan/EDGE-DETECTION/assets/138849336/0c1e0ce3-e685-40d7-91c9-ce5fd2bcb199)

### Sobel XY
![image](https://github.com/Abburehan/EDGE-DETECTION/assets/138849336/b577f259-e0b5-462b-961a-55729bcd41b1)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Abburehan/EDGE-DETECTION/assets/138849336/7cfda654-c91f-42cc-92cc-693b09e0d6b8)

### CANNY EDGE DETECTOR
![image](https://github.com/Abburehan/EDGE-DETECTION/assets/138849336/7e61b858-b9f9-498d-9410-c6b4eb8bfa91)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
