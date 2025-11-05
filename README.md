# EXP 09 : Implementation of Erosion and Dilation
### NAME : MUKESH KUMAR S
### REGISTER NO : 212223240099

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
 
## Algorithm:
### Step1: 
Import OpenCV and NumPy packages.
<br>


### Step2:
Create an image with text using cv2.putText().
<br>

### Step3: 
Create a structuring element (kernel) to perform morphological operations.
<br>

### Step4:
Apply erosion to the text image using cv2.erode().
<br>

### Step5: 
Apply dilation to the text image using cv2.dilate().
<br>

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the text using cv2.putText
img = np.zeros((200, 600), dtype=np.uint8)
cv2.putText(img, "OPEN CV", (50, 120), cv2.FONT_HERSHEY_SIMPLEX, 4, (255), 15)

# Create the structuring element
kernel = np.ones((5, 5), np.uint8)

# Erode the image
eroded_img = cv2.erode(img, kernel, iterations=1)

# Dilate the image
dilated_img = cv2.dilate(img, kernel, iterations=1)

# Display images
plt.figure(figsize=(10,4))

plt.subplot(1,3,1)
plt.title("Input Image")
plt.imshow(img, cmap='gray')
plt.axis('off')

plt.subplot(1,3,2)
plt.title("Eroded Image")
plt.imshow(eroded_img, cmap='gray')
plt.axis('off')

plt.subplot(1,3,3)
plt.title("Dilated Image")
plt.imshow(dilated_img, cmap='gray')
plt.axis('off')

plt.show()


```
## Output:

### Displaying the input Image, Eroded Image and Dilated Image

<img width="1063" height="173" alt="Screenshot 2025-11-04 190446" src="https://github.com/user-attachments/assets/19cb83d2-6932-4c40-a162-689128333240" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
