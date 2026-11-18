# IMPLEMENTATION-OF-EROSION-AND-DILATION

## Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

~~~python

import cv2
import numpy as np
import matplotlib.pyplot as plt

img = np.zeros((300, 500), dtype=np.uint8)

cv2.putText(img, 'EROSION', (50, 140),
            cv2.FONT_HERSHEY_SIMPLEX, 2, 255, 5)

kernel = np.ones((5, 5), np.uint8)

erosion = cv2.erode(img, kernel, iterations=1)
dilation = cv2.dilate(img, kernel, iterations=1)

plt.figure(figsize=(10, 4))

plt.subplot(1, 3, 1)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 3, 2)
plt.imshow(erosion, cmap='gray')
plt.title('Erosion')
plt.axis('off')

plt.subplot(1, 3, 3)
plt.imshow(dilation, cmap='gray')
plt.title('Dilation')
plt.axis('off')

plt.show()

~~~

## Developed By

**Name:** Tharun S

**Register No:** 212225240174

## Output

<img width="1482" height="392" alt="Screenshot 2026-11-17 091308" src="https://github.com/user-attachments/assets/4bf5cd40-b2df-4be0-9bb4-bc2a88518e5e" />



### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.

### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
