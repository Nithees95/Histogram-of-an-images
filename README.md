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


# Developed By: NITHEESH YEGAVINTI
# Register Number: 212224040370

## Program and output:

### Input Grayscale Image and Color Image
```
import cv2
from matplotlib import pyplot as plt
#Load the color image
image = cv2.imread("C:\\Users\\admin\\Downloads\\African_Bush_Elephant.jpg")
#Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
   <img width="816" height="552" alt="image" src="https://github.com/user-attachments/assets/ded16ac5-0f90-444b-9e1a-13ac74c5cf5e" />


### Histogram of Grayscale Image and any channel of Color Image

```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
.    <img width="883" height="602" alt="image" src="https://github.com/user-attachments/assets/b2ef7e5b-e3f3-440b-af32-c4d165d2b46b" />

## Equalised Image 
        
```
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```

<img width="778" height="553" alt="image" src="https://github.com/user-attachments/assets/ffa5e2d9-d346-4455-8138-bd1db782f53e" />

### Histogram Equalization of Grayscale Image.

```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
<img width="816" height="602" alt="image" src="https://github.com/user-attachments/assets/8bdb80b0-1bc2-4a6b-a494-35835bf38c1f" />




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
