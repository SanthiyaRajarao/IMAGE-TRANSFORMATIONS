# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import numpy module as np and pandas as pd.

### Step2:
<br>Assign the values to variables in the program.
### Step3:
<br>Get the values from the user appropriately.


### Step4:
<br>Continue the program by implementing the codes of required topics.

### Step5:
<br>Thus the program is executed in jupyter notebook.

## Program:
python
Developed By: SANTHIYA R
Register Number: 212223230192
### i)Image Translation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

img = cv2.imread('mountain.jpg')

plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB)) 
plt.title("Original Image")  
plt.axis('off')

tx, ty = 50, 10
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])
translated_img = cv2.warpAffine(img, M_translation, (img.shape[1], img.shape[0]))  

plt.imshow(cv2.cvtColor(translated_img, cv2.COLOR_BGR2RGB))
plt.title("Translated Image")  
plt.axis('off')
```

### ii) Image Scaling
```
fx, fy = 4.0, 2.0  
scaled_image = cv2.resize(img, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)

plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  
plt.title("Scaled Image")
plt.axis('off')
```


### iii)Image shearing
```
shear_matrix = np.float32([[1, 0.5, 0], [0.3, 1, 0]])  
sheared_image = cv2.warpAffine(img, shear_matrix, (img.shape[1], img.shape[0]))
plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))
plt.title("Sheared Image") 
plt.axis('off')
```


### iv)Image Reflection
```
reflected_image = cv2.flip(img, 2)
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))  
plt.title("Reflected Image")
plt.axis('off')
```


### v)Image Rotation
```
(height, width) = img.shape[:2] 
angle = 90
center = (width // 2, height // 2) 
M_rotation = cv2.getRotationMatrix2D(center, angle, 1) 
rotated_image = cv2.warpAffine(img, M_rotation, (width, height))  
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image") 
plt.axis('off')
```



### vi)Image Cropping

```
x, y, w, h = 100, 100, 200, 150 
cropped_image = img[y:y+h, x:x+w]
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB)) 
plt.title("Cropped Image")
plt.axis('off')
```

## Output:
### i)Original Image
![Screenshot 2025-04-11 110720](https://github.com/user-attachments/assets/a1d0d69c-bb77-4a48-9266-49eca95fea95)


### i)Image Translation
![Screenshot 2025-04-11 110727](https://github.com/user-attachments/assets/97c4bcb6-e01e-4816-9bbe-b3c4f87501fe)


### ii) Image Scaling
![Screenshot 2025-04-11 110734](https://github.com/user-attachments/assets/63c5836f-929f-47f3-b94d-4da4069b82ea)



### iii)Image shearing
![Screenshot 2025-04-11 110741](https://github.com/user-attachments/assets/39f4e03a-e8c7-4512-8977-143f514c03f5)



### iv)Image Reflection
![Screenshot 2025-04-11 110748](https://github.com/user-attachments/assets/2b612b5c-cd02-4028-a27a-f66c16ebfa41)

### v)Image Rotation
![Screenshot 2025-04-11 110757](https://github.com/user-attachments/assets/ea81aa5b-1080-4509-9c0b-50b3870b4d2d)




### vi)Image Cropping
![Screenshot 2025-04-11 110804](https://github.com/user-attachments/assets/4ff2dd23-d647-4280-8e63-bfd9f19e44cb)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
