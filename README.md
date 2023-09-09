# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.
<br>

### Step2:
Translate the image.
<br>

### Step3:
Scale the image.
<br>

### Step4:
Shear the image.
<br>

### Step5:
Find reflection of image.
<br>
## Step6:
Rotate the image.
<br>
## Step7:
Crop the image.
<br>
## Step8:
Display all the Transformed images.
<br>
## Program:
```python
Developed By:Kavinesh M
Register Number:212222230064
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
c_image = cv2.imread("dt4.jpg")
c_image = cv2.cvtColor(c_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(c_image)
plt.show()
rows,cols,dim = c_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()

ii) Image Scaling
rows,cols,dim = c_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img = cv2.warpPerspective(c_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()


iii)Image shearing
rows,cols,dim = c_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()

iv)Image Reflection
rows,cols,dim = c_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(c_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(c_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

v)Image Rotation
rows,cols,dim = c_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(c_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping
rows,cols,dim = c_image.shape
cropped_img=c_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation
![image](https://github.com/kavinesh8476/IMAGETRANSFORMATION/assets/118466561/cd231339-8ccf-4da3-8197-24fe4642a8cc)

<br>

### ii) Image Scaling
![image](https://github.com/kavinesh8476/IMAGETRANSFORMATION/assets/118466561/49da3af8-03ee-4196-be21-3394ac53f418)
<br>

### iii)Image shearing
![image](https://github.com/kavinesh8476/IMAGETRANSFORMATION/assets/118466561/5563c582-d4f4-485c-bb75-785464caaf7c)

<br>

### iv)Image Reflection
![image](https://github.com/kavinesh8476/IMAGETRANSFORMATION/assets/118466561/f2338aa8-4d32-4fab-8db1-27801a6b1267)

<br>

### v)Image Rotation
![image](https://github.com/kavinesh8476/IMAGETRANSFORMATION/assets/118466561/569fdf41-4f2c-4dc3-bb10-3df59a5e22da)

<br>

### vi)Image Cropping
![image](https://github.com/kavinesh8476/IMAGETRANSFORMATION/assets/118466561/e5998e03-0a4d-45a3-bcb6-52da6c2fe512)

<br>

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
