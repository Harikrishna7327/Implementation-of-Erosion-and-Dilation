# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.

 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np

# Create the Text using cv2.putText
img1 = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Hari krishna',(5,70),font,2,(255),5,cv2.LINE_AA)


# Create the structuring element
cv2.imshow("Name Image",img1)


# Erode the image and Dilate the image

kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
erodeImage = cv2.erode(img1,kernel1)
dilationImage = cv2.dilate(img1,kernel1)
cv2.imshow("Erode Image",erodeImage)
cv2.imshow("Dilated Image",dilationImage)
cv2.waitKey(0)

cv2.destroyAllWindows()



```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/94882905/235294467-300a3723-81f4-4428-a283-b196a7cbf0d6.png)


### Display the Eroded Image
![image](https://user-images.githubusercontent.com/94882905/235294522-0933ee84-afdf-4942-8ac3-9360d63b3754.png)



### Display the Dilated Image
![image](https://user-images.githubusercontent.com/94882905/235294568-504f0cc1-ccfa-410d-81ad-a8e57479e78d.png)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
