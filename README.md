# workshop3 

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
~~~
import cv2
import numpy as np
import matplotlib.pyplot as plt
~~~
~~~
image = cv2.imread('doggy.jpg')
~~~
~~~
resized = cv2.resize(image, (600, 400))
~~~
~~~
plt.subplot(1, 1, 1)
plt.title('Original')
plt.imshow(cv2.cvtColor(resized, cv2.COLOR_BGR2RGB))
plt.axis('off')
~~~

<img width="678" height="477" alt="image" src="https://github.com/user-attachments/assets/9416aded-df66-4625-8299-42e7d42a95ca" />

~~~
gray = cv2.cvtColor(resized, cv2.COLOR_BGR2GRAY)
~~~

~~~
plt.subplot(1, 1, 1)
plt.title('Grayscale Image')
plt.imshow(gray, cmap='gray')
plt.axis('off')
~~~

<img width="742" height="463" alt="image" src="https://github.com/user-attachments/assets/ac252263-2c87-498f-aac1-b7a928d6766d" />

~~~
blur = cv2.GaussianBlur(gray, (5, 5), 1.4)
~~~
~~~
plt.subplot(1, 1, 1)
plt.title('Gaussian Blurred Image')
plt.imshow(blur, cmap='gray')
plt.axis('off')
~~~

<img width="733" height="455" alt="image" src="https://github.com/user-attachments/assets/29fba0b1-08ae-45da-ad52-d932743e85d1" />

~~~
edges = cv2.Canny(blur, 100, 200)
~~~
~~~
plt.subplot(1, 1, 1)
plt.title('Canny Edge Detection')
plt.imshow(edges, cmap='gray')
plt.axis('off')
~~~

<img width="737" height="456" alt="image" src="https://github.com/user-attachments/assets/4b9096c6-3be1-4b5f-ae87-5eeafa290e2f" />



# Result :
The program successfully converts the original image into grayscale and detects edges using the Canny Edge Detection method.
