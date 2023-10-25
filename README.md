# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

Import the required packages for further process.

### Step2:
<br>

Read the image and convert the rgb image to gray scale image.

### Step3:
<br>

Use filters for smoothing the image to reduce the noise.

### Step4:
<br>

Apply the respective filters - Sobel, Laplacian edge detector and Canny edge detector.

### Step5:
<br>

Display the filtered image using plot and imshow.

## Program:
```
DEVELOPED BY: G.Lutheesh
REGISTER NUMBER:212221230029
```
## Import the packages

``` Python
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("thala.jpg")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```
## SOBEL EDGE DETECTOR
## SOBEL X:
```python
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()
```
SOBEL Y:
```python
sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()
```
SOBEL XY:
```python
sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()
```
## LAPLACIAN EDGE DETECTOR
```python
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()

```
## CANNY EDGE DETECTOR

```python
canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()

```


## Output:
### SOBEL EDGE DETECTOR
# SOBEL X:


![WhatsApp Image 2023-10-25 at 10 38 16_58cc6f66](https://github.com/Lutheeshgoparapu/EDGEDETECTION/assets/94154531/9e98849c-513a-43ef-87b5-c2e6e4c15a64)


# SOBEL Y:

![WhatsApp Image 2023-10-25 at 10 38 26_12b07916](https://github.com/Lutheeshgoparapu/EDGEDETECTION/assets/94154531/ea59deff-b334-4dfb-82f9-f59e467ac933)


# SOBEL XY:


![WhatsApp Image 2023-10-25 at 10 38 39_048ed5c3](https://github.com/Lutheeshgoparapu/EDGEDETECTION/assets/94154531/2566a471-d3b2-4a20-9735-5c3b6e3685e3)



### LAPLACIAN EDGE DETECTOR




![WhatsApp Image 2023-10-25 at 10 38 49_7dc0b4b5](https://github.com/Lutheeshgoparapu/EDGEDETECTION/assets/94154531/08dc0fc9-e4bc-4554-affa-e11f6ebb8a4b)


### CANNY EDGE DETECTOR

![WhatsApp Image 2023-10-25 at 10 39 01_47e326d4](https://github.com/Lutheeshgoparapu/EDGEDETECTION/assets/94154531/f4300dde-a208-4592-bcf7-962b07bf5414)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
