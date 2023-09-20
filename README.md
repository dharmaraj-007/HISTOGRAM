# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and matplotlib.pyplot
<br>

### Step2:
Read and display the input images
<br>

### Step3:
Calculate the Histogram Values using calcHist()
<br>

### Step4:
Display the histograms
<br>

### Step5:
Calculate and display the equalized image using equalizeHist()
<br>


## Program:
```python
# Developed By:Dharmaraj S
# Register Number:212222240025
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

import cv2
import matplotlib.pyplot as plt

gray_image = cv2.imread('eagle.png')
color_image = cv2.imread('birds.png')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()



# Display the histogram of gray scale image and any one channel histogram from color image

hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()


# Write the code to perform histogram equalization of the image. 

Gray_image=cv2.imread('fruit.png',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![1](https://github.com/dharmaraj-007/HISTOGRAM/assets/119560386/167083fd-c93b-42e2-bb5e-a9076eab0674)
![2](https://github.com/dharmaraj-007/HISTOGRAM/assets/119560386/33b24db9-8154-4d0d-bce3-67a91cf736e7)

### Histogram of Grayscale Image and any channel of Color Image
![3](https://github.com/dharmaraj-007/HISTOGRAM/assets/119560386/861b7417-d0b8-4e6d-bff8-bdf43677505f)
![4](https://github.com/dharmaraj-007/HISTOGRAM/assets/119560386/8cdb7e24-4716-4117-8b9f-22e9d0becb9d)

### Histogram Equalization of Grayscale Image
![5](https://github.com/dharmaraj-007/HISTOGRAM/assets/119560386/e7b89442-c612-4909-8fdb-dfcdae7429a8)

![7](https://github.com/dharmaraj-007/HISTOGRAM/assets/119560386/3f7fc1bf-3ca3-4707-b418-6c9873dc74e5)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
