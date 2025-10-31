# Workshop3

# Aim:

To implement Canny Edge Detection using Python and OpenCV to detect edges in an image.

# Algorithm:

1.Read the original image from the input source using OpenCV.

2.Display the original image to visualize the input before processing.

3.Convert the image to grayscale using cv2.cvtColor() to simplify the edge detection process.

4.Apply Gaussian Blur to the grayscale image to remove noise and smoothen it.

5.Apply Canny Edge Detection using cv2.Canny() to detect the edges in the image.

6.Display the grayscale image and edge-detected image to compare the results.

# Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
image = cv2.imread('doggy.jpg')
```
```
resized = cv2.resize(image, (600, 400))
```
```
plt.subplot(1, 1, 1)
plt.title('Original')
plt.imshow(cv2.cvtColor(resized, cv2.COLOR_BGR2RGB))
plt.axis('off')
```
<img width="482" height="512" alt="image" src="https://github.com/user-attachments/assets/82b2c84a-50e0-40d6-a500-49327f540591" />

```
gray = cv2.cvtColor(resized, cv2.COLOR_BGR2GRAY)
```
```
plt.subplot(1, 1, 1)
plt.title('Grayscale Image')
plt.imshow(gray, cmap='gray')
plt.axis('off')
```
<img width="505" height="510" alt="image" src="https://github.com/user-attachments/assets/dca1d75c-1b99-4940-84be-d839e6ff7f0c" />
```
blur = cv2.GaussianBlur(gray, (5, 5), 1.4)
```
```
plt.subplot(1, 1, 1)
plt.title('Gaussian Blurred Image')
plt.imshow(blur, cmap='gray')
plt.axis('off')
```
<img width="491" height="506" alt="image" src="https://github.com/user-attachments/assets/a0d521c8-c67c-4f29-b817-294c121e84df" />

```
edges = cv2.Canny(blur, 100, 200)
```
```
plt.subplot(1, 1, 1)
plt.title('Canny Edge Detection')
plt.imshow(edges, cmap='gray')
plt.axis('off')
```
<img width="497" height="501" alt="image" src="https://github.com/user-attachments/assets/51d4ee7f-e509-4629-9134-4883c7f8b1c0" />

# Result :

The program successfully converts the original image into grayscale and detects edges using the Canny Edge Detection method.
