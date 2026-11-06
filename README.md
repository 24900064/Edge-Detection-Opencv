# Edge-Detection-Opencv

## Aim

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

---

## Software Required

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

## ⚙️ Algorithm

### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load an image using `cv2.imread()`.

### Step 3:
Convert the image to grayscale.

### Step 4:
Apply **Original Image** using OpenCV to detect edges.

### Step 5:
Apply **Sobel Edge Detector** using custom kernels.

### Step 6:
Apply **Laplacian operator** using OpenCV.

### Step 7:
Apply **Canny edge detector** using OpenCV.

### Step 8:
Display all edge-detected images for comparison.

---

## Developed By

- **Name:** PRAGATHEESHRAAJ D
- **Register No:** 212224230199  

---

## Output

###  Original Image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('pragatheeshraaj.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="380" height="437" alt="image" src="https://github.com/user-attachments/assets/93829900-5f57-4ad7-996e-f29bcf558cae" />


###  Sobel Edge Detector
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="361" height="436" alt="image" src="https://github.com/user-attachments/assets/2b013193-0c4c-46fb-b06f-8f1eb0870fef" />



###  Laplacian Edge Detector
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="332" height="435" alt="image" src="https://github.com/user-attachments/assets/16dc529e-713b-4acf-9cfd-95b6fd268c03" />


###  Canny Edge Detector
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
<img width="312" height="427" alt="image" src="https://github.com/user-attachments/assets/049f55f2-539f-4390-96b4-e530a7e9c8b2" />


## Result

Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
