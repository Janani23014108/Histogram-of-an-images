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

## Developed By: J.JANANI
## Register Number: 212223230085

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('iron.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])



plt.subplot(2, 2, 4)
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()


```


## Output:
### Input Grayscale Image and Color Image

![437145284-202e3ef5-01ef-4830-a932-54360e3d286d](https://github.com/user-attachments/assets/cec8f6aa-b087-402b-9fcf-28f9000c10a1)


### Histogram of Grayscale Image and any channel of Color Image
![437145509-09009f4d-23d5-430c-8240-832eab07f222](https://github.com/user-attachments/assets/a5fe040c-150c-4f87-a4bb-59dd309df3dc)



### Histogram Equalization of Grayscale Image.

![437145724-5bfe5930-fe11-498a-a061-605e7d90f89e](https://github.com/user-attachments/assets/e587b4e4-7b35-4cbe-9136-2e3ef6579782)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
