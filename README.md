
## Aim
To implement Opening and Closing using Python and OpenCV.

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
Use Opening operation.

### Step5:
Use Closing Operation.

## Program:
### Name:SABARINATH R
### Register Number: 212223100048
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt

def load_img():
    blank_img = np.zeros((300,700), dtype=np.uint8)
    front = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='SABARI', org=(50,200), fontFace=front, 
                fontScale=5, color=(255, 255, 255), thickness=25, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img,title="Original Image"):
    fig=plt.figure(figsize=(10,8))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    ax.set_title(title, fontsize=16)
    plt.show()

img = load_img()
display_img(img)
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (12,12))

image=load_img()
opening_img = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
display_img(opening_img,"Opening Image")

image=load_img()
closing_img = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
display_img(closing_img,"Closing Image")
```
## Output:
### Display the input Image
![image](https://github.com/user-attachments/assets/537d4b59-2bb5-42b0-a644-20a8e511d1e9)


### Display the result of Opening
![image](https://github.com/user-attachments/assets/cdb10693-5a93-40ac-80d1-85cfed3a3820)


### Display the result of Closing
![image](https://github.com/user-attachments/assets/899d683a-b5f7-4a66-a4c8-7a7c3707d309)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.


