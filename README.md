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
## PROGRAM:
```
 DEVELOPED BY:SIVABALAN S
 REGISTER NUMBER: 212222240100
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("ed.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
## SOBEL X:
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
## SOBEL Y:
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## SOBEL XY:
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:

![ed](https://github.com/sivabalan28/EDGE-DETECTION/assets/113497347/2a8eadd1-4712-480c-aa61-9ca0f11ac3ac)

### SOBEL EDGE DETECTOR:

![Screenshot 2024-04-02 222530](https://github.com/sivabalan28/EDGE-DETECTION/assets/113497347/07bfcb8f-839b-4a4e-aade-73f41012f5cc)

![Screenshot 2024-04-02 222539](https://github.com/sivabalan28/EDGE-DETECTION/assets/113497347/386bad50-405b-425d-85c3-eefe45fdb984)

![Screenshot 2024-04-02 222552](https://github.com/sivabalan28/EDGE-DETECTION/assets/113497347/42cddd73-5ebe-4d43-b2ba-5f95faf9a68c)

### LAPLACIAN EDGE DETECTOR

![Screenshot 2024-04-02 222607](https://github.com/sivabalan28/EDGE-DETECTION/assets/113497347/ac2df5a6-9fad-4b4d-adff-cd3f0847f4a5)

### CANNY EDGE DETECTOR
![Screenshot 2024-04-02 222615](https://github.com/sivabalan28/EDGE-DETECTION/assets/113497347/10526555-9cd5-45e7-8808-609e18189aa9)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
