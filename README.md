# Histogram of an images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Read the gray and color image using imread()

### Step 2:
Print the image using imshow().

### Step 3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step 4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step 5:
The Histogram of gray scale image and color image is shown.


## Program :

## Developed By : Yathin Reddy T
## Register Number : 212223100062

## Input Grayscale Image :
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('image.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```

## Histogram of Grayscale Image :

```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```

## Equalization :

```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```

## Equalized Histogram :

```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```






## Output:
### Input Grayscale Image and Color Image

![image](https://github.com/user-attachments/assets/517c4389-6515-4db0-8259-3c8fcebc5d2d)

### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/user-attachments/assets/4923ce01-736c-4f8b-b3ac-c7c25d5cc5e3)

### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/2431e030-06b6-4492-8299-1bb4e8d30a7d)

### Equalized Histogram. 

![image](https://github.com/user-attachments/assets/8615c4b4-b7a6-4ac2-bc1b-1b21ea14421d)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
