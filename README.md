#10. Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
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
Erode and Dilate the image.
### Step5:
End Program.


 
## Program:

``` Python
import cv2
import matplotlib.pyplot as plt
import numpy as np

image1 = np.zeros((100,450), dtype = 'uint8')
image1 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_TRIPLEX = 3
cv2.putText(image1,'soundariyan',(5,70),font,2, (0,225,0),5,cv2.LINE_AA)

plt.figure()
plt.imshow(image1)
plt.title("original image")
plt.axis("off")
plt.show()

kernel = np.ones((5,5),np.uint)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(2,9))
image_erode1 = cv2.erode(image1,kernel1)
image_dilation  = cv2.dilate(image1, kernel1)

plt.figure()
plt.imshow(image_erode1)
plt.title("erosion")
plt.axis("off")
plt.show()

plt.figure()
plt.imshow(image_dilation)
plt.title("dilation")
plt.axis("off")
plt.show()
```


## Output:

### Display the input Image
![model](out.1.png)

### Display the Eroded Image
![model](out.2.png)

### Display the Dilated Image
![model](out.3.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
