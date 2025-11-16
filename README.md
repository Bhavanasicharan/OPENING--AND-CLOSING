# OPENING--AND-CLOSING
# Name: B Charan Reddy
# Reg No: 212224240026
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
 Import the necessary packages


### Step2:
 Give the input text using cv2.putText()


### Step3:
 Perform opening operation and display the result


### Step4:
 Similarly, perform closing operation and display the result



 
## Program:

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'CharanReddy',(5,70), font,2,(255),5,cv2.LINE_AA)

```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation

```
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```


# Use Closing Operation
```
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
<br>
<br>
<img width="673" height="109" alt="image" src="https://github.com/user-attachments/assets/b615cc75-7a39-4290-b66c-2c159d46b1f1" />

<br>
<br>
<br>

### Display the result of Opening
<br>
<br>
<br>
<img width="630" height="155" alt="image" src="https://github.com/user-attachments/assets/d64fcd95-8448-4df0-b737-42e638cd5581" />

<br>
<br>

### Display the result of Closing
<br>
<br>
<br>
<img width="639" height="175" alt="image" src="https://github.com/user-attachments/assets/8d04ae85-5abe-4073-96f8-9b76710b512b" />

<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
