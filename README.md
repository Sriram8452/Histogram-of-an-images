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

### Developed By: Sriram G
### Register Number: 212222230149

### Colour and Gray Image:
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('Spb.jpeg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
```
# Load the color image
image = cv2.imread('SPB Dark.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
### Histogram of Grayscale Image:
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
### Histogram Equalization of Grayscale Image:

```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```

## Output:

### Colour and Gray Image
![image](https://github.com/user-attachments/assets/04c800e9-fe25-4e46-833a-f791ed1113f8)
![image](https://github.com/user-attachments/assets/8e686a4e-ea89-4750-9402-1f1b6bf86cbd)



### Histogram of Grayscale Image
![image](https://github.com/user-attachments/assets/d93e87de-61e1-447f-bf90-69ec479095f1)
![image](https://github.com/user-attachments/assets/ef9cb669-cee5-4a5a-8664-4489e970ab1e)


### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/95fa1ecf-2589-459a-90a4-ef8624f1b806)
![image](https://github.com/user-attachments/assets/b3cfda55-cbe4-4e3b-ba40-3600052beea4)

![image](https://github.com/user-attachments/assets/059aa85f-f382-451d-8d89-2723f90da86d)
![image](https://github.com/user-attachments/assets/1720fde5-0ff3-47bc-9364-7927182c514b)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
