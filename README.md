# EXPERIMENT 11:OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Implement Opening Operation.

### Step 5:
Implement Closing Operation.
## PROGRAM:

``` 
# Import the necessary packages
import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText
text_image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Rithiga Sri.B",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')

# Use Closing Operation
closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')

```
## OUTPUT:
* Display the input Image:  
![image](https://github.com/Rithigasri/Opening-and-Closing/assets/93427256/64f00362-5bf7-4155-9c24-416a619b0770)

* Display the result of Opening:  
![image](https://github.com/Rithigasri/Opening-and-Closing/assets/93427256/226f492e-ff67-478a-a3a2-ae37529417b2)

* Display the result of Closing:  
![image](https://github.com/Rithigasri/Opening-and-Closing/assets/93427256/8db4ad3f-bfa3-415c-b447-3ddfda0d31ee)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
