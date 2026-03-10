# EXP-8-THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale
### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.
## Program
NAME : HARISH D

REG NO : 212224220034

```python
# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt




# Read the Image and convert to grayscale
# Step 2: Read the image and convert to grayscale
image = cv2.imread('harish.tif')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale




# Use Global thresholding to segment the image

plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')


# Use Adaptive thresholding to segment the image


# Step 3: Use Global Thresholding to segment the image
# Apply global thresholding with a threshold value of 127
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

# Use Otsu's method to segment the image 

# Step 4: Use Adaptive Thresholding to segment the image
# Apply adaptive thresholding using Gaussian method
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)



# Display the results
# Step 5: Use Otsu's method to segment the image
# Apply Otsu's method for optimal thresholding
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

# Global Thresholding
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

# Show the plot
plt.tight_layout()
plt.show()



```
## Output

### Original Image
<br>
<br><img width="773" height="302" alt="image" src="https://github.com/user-attachments/assets/8a342e51-9445-4949-be20-077c13fa8615" />

<br>
<br>
<br>

### Global Thresholding
<br>
<br>
<br>
<br><img width="825" height="595" alt="image" src="https://github.com/user-attachments/assets/082ce0cd-6bfb-41eb-b872-9fc66cdfa379" />

<br>

### Adaptive Thresholding
<br>
<br>
<br><img width="825" height="595" alt="image" src="https://github.com/user-attachments/assets/5f1256a9-c80a-41e2-b854-7a194b1e1ec9" />

<br>
<br>

### Optimum Global Thesholding using Otsu's Method
<br>
<br>
<br><img width="825" height="595" alt="image" src="https://github.com/user-attachments/assets/80c66ff1-4ec5-42ed-ba86-26f0de8040f7" />

<br>
<br>


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
