# Implementation-of-Filters...

## Aim:

To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:

Anaconda - Python 3.7 .

## Algorithm:

### Step 1:

Import cv2, matplotlib.py libraries and read the saved images using cv2.imread().

### Step 2:

Convert the saved BGR image to RGB using cvtColor().

### Step 3:

By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator.

### Step 4:

Apply the filters using cv2.filter2D() for each respective filters.

### Step 5:

Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().

## Program:

```python

### Developed By : Anto Richard .S
### Register Number : 212221240005

```

### 1. Smoothing Filters:

i) Using Averaging Filter:

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('sam.jpeg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel = np.ones ((11,11), np.float32)/121
image3=cv2.filter2D(image2,-1, kernel)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')


```


ii) Using Weighted Averaging Filter:

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('sam.jpeg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16 
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')


```


iii) Using Gaussian Filter:

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('sam.jpeg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(11,11),sigmaX=0,sigmaY=0)
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16 
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

```


iv) Using Median Filter:

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('sam.jpeg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
median=cv2.medianBlur(src=image2, ksize=11)
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16 
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

```


### 2. Sharpening Filters:

i) Using Laplacian Kernal:

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('sam.jpeg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel3=np.array([[0,1,0],[1,-4,1],[0,1,0]])
image3=cv2.filter2D(image2,-1, kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

```


ii) Using Laplacian Operator:

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('sam.jpeg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
new_image = cv2.Laplacian(image2, cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(new_image)
plt.title('Filtered')
plt.axis('off')

```

## OUTPUT:

### 1. Smoothing Filters:


i) Using Averaging Filter:

![out1](https://user-images.githubusercontent.com/93427534/230780468-a376a039-1803-464b-b3cd-dbd96c344f00.png)

ii) Using Weighted Averaging Filter:

![out2](https://user-images.githubusercontent.com/93427534/230780474-ea0f58d1-e57b-472d-8a3f-aef0c5fcd859.png)

iii) Using Gaussian Filter:

![out3](https://user-images.githubusercontent.com/93427534/230780480-ab8882d3-3e99-4fb9-ab3e-9e9ea5b61879.png)

iv) Using Median Filter:

![out4](https://user-images.githubusercontent.com/93427534/230780482-2ae08133-dd8b-4f8f-be49-9f1030781113.png)

### 2. Sharpening Filters:


i) Using Laplacian Kernal:

![out5](https://user-images.githubusercontent.com/93427534/230780488-be84f474-318c-4e04-9b99-425561b446ee.png)

ii) Using Laplacian Operator:

![out6](https://user-images.githubusercontent.com/93427534/230780495-e5e07764-ea4b-4372-be9d-3697f2d8993f.png)

## Result:

Thus the filters are designed for smoothing and sharpening the images in the spatial domain.


