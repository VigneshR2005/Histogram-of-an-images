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

# Load the color image
image = cv2.imread('dog.jpg')

# Convert the image to grayscale
gray_image = c
v2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

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
### Input Grayscale Image and Color Image
![Screenshot 2024-10-01 103659](https://github.com/user-attachments/assets/025f9cce-da4d-4a04-8018-7a06508da8c2)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-10-01 103732](https://github.com/user-attachments/assets/e69e0f21-b661-4b8f-8f61-84f0fe121555)



### Histogram Equalization of Grayscale Image.
![Screenshot 2024-10-01 103753](https://github.com/user-attachments/assets/0dce7c47-8500-4053-a60c-6db8ef3d8c8d)






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
