# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Program:
## Developed by: ROGITH GANESH R
## Register number: 212223100046
## PROGRAM
```

import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'ROGITH GANESH' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')
```

## Output:

### Display the input Image

![Screenshot 2025-05-17 054946](https://github.com/user-attachments/assets/4f709d14-0e58-43c7-a054-e44deff6df04)


### Display the Eroded Image
![Screenshot 2025-05-17 054952](https://github.com/user-attachments/assets/5c4640e8-8429-48dd-baf8-55a0bab3df1f)



### Display the Dilated Image
![image](https://github.com/user-attachments/assets/368077ea-d317-427e-810a-f96a571a3b96)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
