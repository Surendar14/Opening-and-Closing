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
![1](https://user-images.githubusercontent.com/75235759/175002123-7635f777-29c3-47e0-9a31-ff46b210997d.png)

### Opening
![2](https://user-images.githubusercontent.com/75235759/175002161-ca265766-ef70-4609-9730-2f5e374b9ddf.png)


### Closing
![3](https://user-images.githubusercontent.com/75235759/175002244-9f504883-6ab3-42b8-96cd-fd5e8b9f06ec.png)


## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
