
# OPENING--AND-CLOSING
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
### DEVELOPED BY: AHALYA S
### REGISTER NO: 212223230006

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'AHALYA', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```
## Output:

### Display the input Image

<img width="800" height="178" alt="image" src="https://github.com/user-attachments/assets/b40d503b-9f53-46ae-b809-8fbb7e2558f3" />




### Display the result of Opening


<img width="774" height="193" alt="image" src="https://github.com/user-attachments/assets/29835de4-19f2-4da3-8794-c6c3d7fb63e0" />



### Display the result of Closing

<img width="825" height="192" alt="image" src="https://github.com/user-attachments/assets/26fddc32-f2ef-44c1-bb15-ddf89335cd1e" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
