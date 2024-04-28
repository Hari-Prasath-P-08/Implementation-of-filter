# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step 1:
Import the required libraries.

### Step2:
Convert the image from BGR to RGB.

### Step 3:
Apply the required filters for the image separately.

### Step 4:
Plot the original and filtered image by using matplotlib.pyplot.

### Step 5:
End the program.

## Program:

### Developed By: Hari Prasath. P
### Register Number: 212223230070

### 1. Smoothing Filters:

#### i) Using Averaging Filter:

```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('Vikram.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)
kernel = np.ones((11,11), np.float32)/121
image3 = cv2.filter2D(image2,-1, kernel)
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

#### ii) Using Weighted Averaging Filter:

```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('Vikram.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3 = cv2.filter2D(image2,-1, kernel2)
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

#### iii) Using Gaussian Filter:

```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image1 = cv2.imread('Vikram.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)  # Convert BGR to RGB
image3 = cv2.GaussianBlur(src=image2, ksize=(11,11), sigmaX=0, sigmaY=0)

plt.figure(figsize=(9, 9))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

plt.show()
```

#### iv) Using Median Filter:

```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image1 = cv2.imread('Vikram.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)  # Convert BGR to RGB
median = cv2.medianBlur(src=image2, ksize=11)
plt.figure(figsize=(9, 9))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

plt.show()
```

### 2. Sharpening Filters

#### i) Using Laplacian Kernal:

```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image1 = cv2.imread('Vikram.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)  # Convert BGR to RGB
kernel3=np.array([[0,1,0],[1,-4,1],[0,1,0]])
image3=cv2.filter2D(image2,-1,kernel3)

plt.figure(figsize=(9, 9))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

plt.show()
```

#### ii) Using Laplacian Operator:

```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image1 = cv2.imread('Vikram.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)  # Convert BGR to RGB
new_image=cv2.Laplacian(image2,cv2.CV_64F)

plt.figure(figsize=(9, 9))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

plt.show()
```

## OUTPUT:

### 1. Smoothing Filters:

#### i) Using Averaging Filter:

![image](https://github.com/Hari-Prasath-P-08/Implementation-of-filter/assets/139455593/da138a38-bac4-4686-b641-0b670d01b241)

#### ii) Using Weighted Averaging Filter:

![image](https://github.com/Hari-Prasath-P-08/Implementation-of-filter/assets/139455593/23d60cad-fac5-4315-9b3d-0bd54039fc7f)

#### iii) Using Gaussian Filter:

![image](https://github.com/Hari-Prasath-P-08/Implementation-of-filter/assets/139455593/32b552a1-6c3f-4123-900c-cbe7ecf4b632)

#### iv) Using Median Filter:

![image](https://github.com/Hari-Prasath-P-08/Implementation-of-filter/assets/139455593/41f76bf1-a76b-4b0e-904b-0c72ed20d63b)

### 2. Sharpening Filters:

#### i) Using Laplacian Kernal:

![image](https://github.com/Hari-Prasath-P-08/Implementation-of-filter/assets/139455593/43fa0856-b5ef-4ca8-a9c7-73fbb02018eb)

#### ii) Using Laplacian Operator:

![image](https://github.com/Hari-Prasath-P-08/Implementation-of-filter/assets/139455593/10114cf4-d235-43d6-8317-ca45cf46714f)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
