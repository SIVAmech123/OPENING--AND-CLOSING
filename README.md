# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Load the input image using cv2.imread().

### Step2:

Define a structuring element (e.g., 5x5 rectangular) using cv2.getStructuringElement().


### Step3:

Perform erosion followed by dilation using cv2.morphologyEx() with the cv2.MORPH_OPEN operation.


### Step4:

Perform dilation followed by erosion using cv2.morphologyEx() with the cv2.MORPH_CLOSE operation.


### Step5:

Use plt.subplot() to show the original, opening, and closing images side by side.


 
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"SIVAKUMAR R",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image
![WhatsApp Image 2025-05-07 at 15 19 25_d97284f2](https://github.com/user-attachments/assets/5e80e79e-400d-421e-a5f8-4a12caff71ff)




### Display the result of Opening
![WhatsApp Image 2025-05-07 at 15 19 25_3652e543](https://github.com/user-attachments/assets/72853dae-6301-4314-8c33-08cf9c724a7d)

### Display the result of Closing
![WhatsApp Image 2025-05-07 at 15 19 25_28ac54eb](https://github.com/user-attachments/assets/88861b4d-4605-453b-9df3-6eb105c0478d)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
