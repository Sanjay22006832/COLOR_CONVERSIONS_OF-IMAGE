# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.
ii) 	Draw Shapes and Add Text.
iii) Image Color Conversion.
iv) Access and Manipulate Image Pixels.
v) Image Resizing
vi) Image Cropping
vii) Image Flipping
viii)	Write and Save the Modified Image

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.

##### Program:
### Developed By: M Sanjay
### Register Number: 212222240090

## Output:

### i)Read and Display an Image
```
import cv2
img=cv2.imread('loki naa.jpg')
cv2.imshow('LOKI',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 214002](https://github.com/user-attachments/assets/013a9f3d-3079-4bba-8650-ea09c7431dfd)
<br>
<br>

### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image.
```
import cv2
img = cv2.imread("loki naa.jpg")
res = cv2.line(img, (0, 0), (1025, 680), (255, 0, 0), 3)
cv2.imshow('LOKI NAA', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 214528](https://github.com/user-attachments/assets/a2b0b581-57b8-4b67-b3a7-cb49a3c3ebf6)

ii)Draw a circle at the center of the image.
```
# Load the image
img = cv2.imread("loki naa.jpg")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 150, (0, 0, 255), 10)

# Display the image with the circle
cv2.imshow('loki naa', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 214742](https://github.com/user-attachments/assets/7fc05cd2-1e2e-46f7-b1f1-338ff6844323)

iii)Draw a rectangle around a specific region of interest in the image.
```
img = cv2.imread("loki naa.jpg")
start=(0,0)
stop=(318,200)
color=(255,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 214921](https://github.com/user-attachments/assets/2f6038e9-8c3a-47ec-a9a1-303741ff8b5d)

iv)Add the text at the bottom of the image.
```
img = cv2.imread("loki naa.JPG")

# Define the text to be added and its position
text = "LET HIM COOK..."
position = (140, 300)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 215103](https://github.com/user-attachments/assets/a2f6f2de-bd4f-4d5f-a7a7-32a20b43270b)
<br>
<br>

### iii)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 215405](https://github.com/user-attachments/assets/6cd8057d-d3f9-4c1f-90ca-333928862ce0)

ii.)Convert the image from RGB to GRAY and display it.
```
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 215429](https://github.com/user-attachments/assets/ddee4c0a-6e51-4d46-aa35-7285ed7f9d7e)

iii.)Convert the image from RGB to YCrCb and display it.
```
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 215458](https://github.com/user-attachments/assets/af36e84f-47e4-49ce-b498-53d095814271)

iv.)Convert the HSV image back to RGB and display it.
```
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 215519](https://github.com/user-attachments/assets/7cbcc615-71fa-4870-98ed-7cf625708ef0)
<br>
<br>

### iv)Access and Manipulate Image Pixels
```
# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 215953](https://github.com/user-attachments/assets/5937ddd6-48e7-4433-b2b0-0119720fde1e)

![Screenshot 2024-09-18 215940](https://github.com/user-attachments/assets/1c5fe924-6258-4277-b76e-2585d8b29c85)
<br>
<br>

### v)Image Resizing
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(img, (300, 400))
cv2.imshow('Original',img)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 220202](https://github.com/user-attachments/assets/8701a8be-f0fb-43e6-b0af-e0ee8ea24f32)
<br>
<br>

### vi)Image Cropping
```
# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 150, 150

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 220244](https://github.com/user-attachments/assets/993aee78-235c-4760-a2bd-65fa4eb9de63)
<br>
<br>

### vii)Image Flipping
i.)Flip the original image horizontally and display it.
```
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 220455](https://github.com/user-attachments/assets/bd60df16-ca83-421c-b8f6-966fca5f529f)

ii.)Flip the original image vertically and display it.
```
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-18 220533](https://github.com/user-attachments/assets/88d12514-1be8-4ffa-8983-4686ced95655)
<br>
<br>

### viii)Write and Save the Modified Image
```
cv2.imwrite('loki naa.jpg',image)
```
### OUTPUT:
![Screenshot 2024-09-18 220715](https://github.com/user-attachments/assets/7cd105c7-37b9-4ed4-b5a3-a0256495fe1d)
<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
