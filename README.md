# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

# Developed By: Sriram G
# Register Number: 212222230149

## Colour and Gray Image

```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("SPB1.jpeg")
color_image = cv2.imread("SPB.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image

```
import numpy as np
import cv2
Gray_image = cv2.imread("SPB1.jpeg")
Color_image = cv2.imread("SPB.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
## Histogram of Green channel of colour Image

```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
## Histogram Equalization of Grayscale Image

```
import cv2
gray_image = cv2.imread("SPB1.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/50e67ca8-fef2-4c0d-819e-868fada1abc0)

### Histogram of Grayscale Image
![image](https://github.com/user-attachments/assets/3e462b6d-c4ec-4d14-b3f0-6a435baa2b7e)


### Histogram of Green channel of Color Image
![image](https://github.com/user-attachments/assets/dcc4de5b-caa6-4976-ad61-f8393a22de2a)


### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/6ae77c39-c80d-4620-98ed-8a4fbb8fe8a4)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
