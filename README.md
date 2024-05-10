# EXP: 9 Implementation-of-Erosion-and-Dilation
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
```
Developed by : LATHISH KANNA.M
Reg No : 212222230073

```

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'HEALTH',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```

# Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```

# Erode the image

```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



# Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image


![326240903-a4d044ee-69bb-4d30-b56a-d22104654891](https://github.com/Kamali22004796/erosion--dilation/assets/120567837/97e8e75d-f8f6-4de6-8025-c58ca8aea249)


### Display the Eroded Image


![326240916-10f30551-cbe1-4963-9a8d-04c2f5ce8ab7](https://github.com/Kamali22004796/erosion--dilation/assets/120567837/0061a23c-bf75-4b65-9166-a575add259b3)


### Display the Dilated Image


![326240928-cb437ddf-d963-4321-90e9-31d2e2eae73d](https://github.com/Kamali22004796/erosion--dilation/assets/120567837/b12d48bc-df33-4da9-bb68-e281fd7808cc)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
