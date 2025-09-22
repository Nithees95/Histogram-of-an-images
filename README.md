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
# Developed By: NITHEESH YEGAVINTI
# Register Number: 212224040370

### Input Grayscale Image and Color Image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat.jpg")
color_image = cv2.imread("bird.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

### Histogram of Grayscale Image 
import numpy as np
import cv2
Gray_image = cv2.imread("cat.jpg")
Color_image = cv2.imread("bird.jpg")
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

###Histogram of Color image
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)

### Histogram Equalization of Grayscale Image.

import cv2
gray_image = cv2.imread("bird.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Output:

Input Grayscale Image and Color Image

<img width="570" height="352" alt="image" src="https://github.com/user-attachments/assets/07a8c156-37ad-400b-a317-1269e0c7bcb6" />

Histogram of Grayscale Image and  any channel of Color Image

<img width="789" height="1025" alt="image" src="https://github.com/user-attachments/assets/0e5887dd-ba61-4459-9df5-e9f665fd50d4" />

<img width="706" height="934" alt="image" src="https://github.com/user-attachments/assets/7b7288eb-604f-484b-a3ed-2c9318aca9f3" />

Histogram Equalization of Grayscale Image.

<img width="439" height="285" alt="image" src="https://github.com/user-attachments/assets/b176afaa-27e7-4266-b31e-b663e793abea" />



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
