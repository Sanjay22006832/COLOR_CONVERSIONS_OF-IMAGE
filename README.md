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
img=cv2.imread('goat.jpg')
cv2.imshow('Thalaivar',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161221](https://github.com/user-attachments/assets/317f422f-8787-48c1-9fd8-ab2aff7a15da)


<br>
<br>

### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image.
```
import cv2
img = cv2.imread("goat.jpg")
res = cv2.line(img, (0, 0), (1025, 680), (255, 0, 0), 3)
cv2.imshow('TVK', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161228](https://github.com/user-attachments/assets/68777943-c65a-4484-860d-ddf214c76583)


ii)Draw a circle at the center of the image.
```
# Load the image
img = cv2.imread("goat.jpg")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 150, (0, 0, 255), 10)

# Display the image with the circle
cv2.imshow('tvk thalaivar', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161313](https://github.com/user-attachments/assets/20b0409c-eb94-4ddf-96f0-8c4cc683d169)


iii)Draw a rectangle around a specific region of interest in the image.
```
img = cv2.imread("goat.jpg")
start=(0,0)
stop=(318,200)
color=(255,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('TVK Thalaivar', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161359](https://github.com/user-attachments/assets/bd780969-97a6-446d-ba8c-7cadd704a556)


iv)Add the text at the bottom of the image.
```
img = cv2.imread("goat.JPG")

# Define the text to be added and its position
text = "THAMIZHAGA VETRI KAZHAGAM"
position = (150, 600)  # Positioning the text at the top-left corner

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
![Screenshot 2024-09-19 161804](https://github.com/user-attachments/assets/749c52e1-e168-4fb1-92bc-1f19c68b2bf5)


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
![Screenshot 2024-09-19 161854](https://github.com/user-attachments/assets/874fdeea-ee00-4404-9d7e-1656324afede)




ii.)Convert the image from RGB to GRAY and display it.
```
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 162023](https://github.com/user-attachments/assets/1ad2e467-e608-483a-8a00-4476b005ada3)


iii.)Convert the image from RGB to YCrCb and display it.
```
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161944](https://github.com/user-attachments/assets/7ee3b154-3126-4e30-ad88-85b1a63eaef9)


iv.)Convert the HSV image back to RGB and display it.
```
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-23 143248](https://github.com/user-attachments/assets/b4c84e35-228b-4f1a-b2df-010121513b41)

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
![Screenshot 2024-09-23 143333](https://github.com/user-attachments/assets/1dee70ef-9b1d-4421-8cd8-8b6cc0120aa3)
![Screenshot 2024-09-23 143340](https://github.com/user-attachments/assets/78e5c580-cf9d-41f9-a075-4d5a20dc74f4)




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
![Screenshot 2024-09-23 143412](https://github.com/user-attachments/assets/890beba0-5d0e-4361-98e3-de95993f6ff9)

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
![Screenshot 2024-09-23 143613](https://github.com/user-attachments/assets/b8766969-c9bd-4143-93e3-579ca67d8974)

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
![Screenshot 2024-09-23 143637](https://github.com/user-attachments/assets/8c517538-682e-4f68-8269-fd70ecee461d)


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
![Screenshot 2024-09-23 143709](https://github.com/user-attachments/assets/e22834e4-d4c4-4ab3-8d1b-2860188923ba)

<br>
<br>

### viii)Write and Save the Modified Image
```
cv2.imwrite('loki naa.jpg',image)
```
### OUTPUT:
![Screenshot 2024-09-23 143806](https://github.com/user-attachments/assets/0ed73861-15d3-4bfa-96d4-2eeb9f9ed89f)

<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
