# Opening-and-Closing

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.
### Step2:
Create the text image using cv2.putText.
### Step3:
Then create the structuring element for opening and closing.
### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.
### Step5:
Plot the images using plt.imshow.
 
## Program:
```
Developed by : Surendar S
Registeration Number:212220230051
```

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Dinesh",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')
# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))
# Use Opening operation
image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')
# Use Closing Operation
image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')
```

## Output:
### Input Image
![SS1](https://user-images.githubusercontent.com/75234807/173192404-3d4898da-3280-4d49-8009-4c81e91b1139.png)

### Opening
![SS2](https://user-images.githubusercontent.com/75234807/173192407-36714a2b-339a-4e0a-af0d-7d91ace9eb2c.png)

### Closing
![SS3](https://user-images.githubusercontent.com/75234807/173192412-428c7aa8-8cea-410e-abd9-4541a6eb0e6a.png)

## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
