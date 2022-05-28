# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

<br><br><br><br><br>

## PROGRAM:
```
/*
Developed by   : S.Dinesh
Register Number: 212220230011
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Dinesh',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## OUTPUT:

### Display the input Image
![image](https://user-images.githubusercontent.com/75235159/170825311-7c717fbb-1edc-49d5-ba81-e6cce7759742.png)

### Display the result of Opening
![image](https://user-images.githubusercontent.com/75235159/170825323-7cb16afb-afa0-423b-b0cc-5556ae8b7f17.png)

### Display the result of Closing
![image](https://user-images.githubusercontent.com/75235159/170825339-9aef03d9-08bc-469f-b1ab-f5efa50f78e7.png)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
