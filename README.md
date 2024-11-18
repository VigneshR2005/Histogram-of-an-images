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
```python
# Developed By: R Vignesh
# Register Number: 212222230172

import cv2
from matplotlib import pyplot as plt

image = cv2.imread('image03.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])


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
### Input Grayscale Image and Color Image
![download](https://github.com/user-attachments/assets/09d6a0ba-d522-4e84-86d4-0425e35cd432)


![dog](https://github.com/user-attachments/assets/20a92b59-ae1f-401f-98dd-193ca6ecf467)




### Histogram of Grayscale Image and any channel of Color Image

![download](https://github.com/user-attachments/assets/13e5193a-b631-49df-b226-b310f2e50172)




### Histogram Equalization of Grayscale Image.

![download](https://github.com/user-attachments/assets/51b04a74-4d74-4024-a820-0d175efb4e89)


![download](https://github.com/user-attachments/assets/b2f04c05-cd8d-40a7-9278-f84779b25b00)








## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
