# Implementation-of-Erosion-and-Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode the image using cv2.erode().

### Step5:
Dilate the image using cv2.dilate().

 
## Program:

```python

# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Load the Image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
# Create the Text using cv2.putText
cv2.putText(img1,'U.SRINIVAS',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')


```
## Output:

### Display the input Image



<img width="448" alt="image" src="https://github.com/srinivas-aids/Implementation-of-Erosion-and-Dilation/assets/93427183/e56d94d3-f59d-4aae-9a91-4c181003a94d">



### Display the Eroded Image




<img width="421" alt="image" src="https://github.com/srinivas-aids/Implementation-of-Erosion-and-Dilation/assets/93427183/6725fd7a-9fe7-4b2e-a74c-e796bc730a2a">


### Display the Dilated Image


<img width="430" alt="image" src="https://github.com/srinivas-aids/Implementation-of-Erosion-and-Dilation/assets/93427183/b59c309f-a6f3-4c93-953f-8dfa1d3ed7b8">


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
