# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>
### Step2:
Create the Text using cv2.putText.
<br>
### Step3:
Create the structuring element.
<br>
### Step4:
Use Opening and Closing Operations
<br>
### Step5:
End Program.
<br>
## Program:
### Developed By    : R ARUNRAJ
### Register Number : 212220230004
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,270),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"ARUN",(5,70),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Display the input Image
![o1](https://user-images.githubusercontent.com/75235747/171269593-c54b019a-0d4e-44a6-a5d3-9d7457f6aaf5.JPG)
### Display the result of Opening
![o2](https://user-images.githubusercontent.com/75235747/171269683-ee5a6574-6960-4b78-88a3-12238e4497b4.JPG)
### Display the result of Closing
![o3](https://user-images.githubusercontent.com/75235747/171269723-2da2edd7-66a7-431c-88cf-43375291321d.JPG)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
