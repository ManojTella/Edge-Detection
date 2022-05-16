# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the required packages.
<br>

### Step2:
Load the image to operate on.
<br>

### Step3:
Convert the image to grayscale image.
<br>

### Step4:
Use Sobel operator along x,y and xy directions.
<br>

### Step5:
Operate the image using Canny Edge operator.
<br>

### Step6:
Operate the image using Canny Edge operator.

### Step7:
Show all the operated images output.

### Step8:
End the program.


## Program:

``` 
# Import the packages
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
image = cv2.imread("parrot.jpeg")
grayImage = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("OriginalImage",image)
cv2.imshow("GrayscaleImage",grayImage)
smoothImage = cv2.GaussianBlur(grayImage,(3,3),0)


# SOBEL EDGE DETECTOR
sobelx = cv2.Sobel(smoothImage,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(smoothImage,cv2.CV_64F,0,1,ksize=5)
sobelxy = cv2.Sobel(smoothImage,cv2.CV_64F,1,1,ksize=5)



# LAPLACIAN EDGE DETECTOR

laplacian = cv2.Laplacian(smoothImage,cv2.CV_64F)



# CANNY EDGE DETECTOR

cannyEdges = cv2.Canny(smoothImage,120,150)

plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(smoothImage,cmap = 'gray')
cv2.imshow("sobelx",sobelx)
cv2.imshow("sobely",sobely)
cv2.imshow("sobelxy",sobelxy)
cv2.imshow("Laplacian",laplacian)
cv2.imshow("Canny Edges",cannyEdges)
plt.title("Original")
plt.xticks([])
plt.yticks([])
plt.show()


```
## Output:
### Importing 
![img1](https://user-images.githubusercontent.com/94883876/168624571-45525acd-f158-4c1d-8721-54f3d9ab0079.jpeg)
![img2](https://user-images.githubusercontent.com/94883876/168624590-a983e3d5-d0e4-4b1f-bbac-d1787ef7be7e.jpeg)
![img3](https://user-images.githubusercontent.com/94883876/168624614-5ae25df4-9859-4de1-aca0-4d38253d40b4.jpeg)

<br>
<br>
<br>





### SOBEL EDGE DETECTOR
![img4](https://user-images.githubusercontent.com/94883876/168624652-75706365-4eda-4a8a-9817-6ec5fd47e351.jpeg)
![img5](https://user-images.githubusercontent.com/94883876/168624676-22c34a86-b7f9-4016-a81e-cc2a7f861ee7.jpeg)
![img6](https://user-images.githubusercontent.com/94883876/168624815-3735408b-7192-4d73-9f67-895d965e6bb4.jpeg)


<br>
<br>
<br>
<br>
<br>
<br>


### LAPLACIAN EDGE DETECTOR
![img7](https://user-images.githubusercontent.com/94883876/168624850-8f254477-b185-4a70-a9a0-c6af92da3852.jpeg)


<br>
<br>
<br>
<br>
<br>
<br>


### CANNY EDGE DETECTOR
![img8](https://user-images.githubusercontent.com/94883876/168624902-78160a95-a2dd-45a6-8815-31b58c8c9f45.jpeg)

<br>
<br>
<br>
<br>
<br>
<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
