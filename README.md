# COLOR_CONVERSIONS_OF-IMAGE.

### Developed by: Anbuselvan S
### Register No: 212223240008
### Date:

## AIM:
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

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
      o Load an image from your local directory and display it.

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


## Program and Output:

#### Developed by: Anbuselvan.S
#### Register No: 212223240008

### i)Read and Display an Image:

```
import cv2

image = cv2.imread('ofc pic 2.jpg') 
cv2.imshow('Original Image(Anbuselvan)', image)
cv2.waitKey(0)
```

![Screenshot 2024-09-16 083051](https://github.com/user-attachments/assets/96e048d3-a02e-4d9c-96f4-6e0f5cf615b0)

### ii)Draw Shapes and Add Text:

#### line:

```
image.shape

cv2.line(image, (0, 0), (1007,978), (255, 0, 0), 5)
cv2.imshow('Image with Drawing(Anbuselvan)', image)
cv2.waitKey(0)
```

![Screenshot 2024-09-23 091603](https://github.com/user-attachments/assets/16bef3d6-a0e0-4fdf-ba6b-90cbe4a45434)

#### circle:

```
cv2.circle(image, (489,500), 50, (0, 255, 0), 5)
cv2.imshow('Image with Drawing(Anbuselvan)', image)
cv2.waitKey(0)
```

![image](https://github.com/user-attachments/assets/ea8a83a1-77cb-4bcf-9874-936bd8cfc2e8)

### Rectangle:

```
cv2.rectangle(image, (200,200), (489,500), (0, 0, 255), 5)
cv2.imshow('Image with Drawing(Anbuselvan)', image)
cv2.waitKey(0)
```

![image](https://github.com/user-attachments/assets/ac26d5fa-5b03-4ddc-97a7-24d06943df67)

#### Text:

```
cv2.putText(image, 'OpenCV Drawing', (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 0), 2)
cv2.imshow('Image with Drawing(Anbuselvan)', image)
cv2.waitKey(0)
```

![image](https://github.com/user-attachments/assets/a3846dfc-f1a1-419a-93f0-295f0025d586)

### iii)Image Color Conversion:

#### HSV image:

```
hsv_image = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
cv2.imshow('HSV Image', hsv_image)
cv2.waitKey(0)
```

![image](https://github.com/user-attachments/assets/75414cec-1907-4509-8d62-656ae5138fb8)

#### Gray image:

```
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imshow('Gray Image', gray_image)
cv2.waitKey(0)
```
![image](https://github.com/user-attachments/assets/fa18c38c-8c76-4e16-a92d-039520c99367)

#### YCrCb image:

```
ycrcb_image = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('YCrCb Image', ycrcb_image)
cv2.waitKey(0)
```

![image](https://github.com/user-attachments/assets/4c647ff0-8b37-4e3d-84c4-d438f63e7101)

#### RGB from HSV:

```
rgb_from_hsv = cv2.cvtColor(hsv_image, cv2.COLOR_HSV2BGR)
cv2.imshow('RGB from HSV', rgb_from_hsv)
cv2.waitKey(0)
```

![image](https://github.com/user-attachments/assets/b3cce76d-ee10-49ed-96d7-4c5088f56abc)

### iv)Access and Manipulate Image Pixels:

```
pixel_value = image[100, 100]
print(f'Pixel value at (100, 100): {pixel_value}')

image[200, 200] = [255, 255, 255]
```

![Screenshot 2024-09-16 083806](https://github.com/user-attachments/assets/76864aa7-fb04-4e23-adcd-a301b2cfa1a0)

### v)Image Resizing:

```
resized_image = cv2.resize(image, (489,500))
cv2.imshow('Resized Image (Half Size)', resized_image)
cv2.waitKey(0)
```

![image](https://github.com/user-attachments/assets/a98bb39b-3963-48b1-bf70-bcb296f41d15)

### vi)Image Cropping:

```
roi = image[100:489, 100:1000]  
cv2.imshow('Cropped ROI', roi)
cv2.waitKey(0)
```

![image](https://github.com/user-attachments/assets/edddfcb3-e915-42df-8900-f50098d84f7d)

### vii)Image Flipping:

#### Horizontal:

```
flipped_horizontally = cv2.flip(image, 1)

cv2.imshow('Flipped Horizontally', flipped_horizontally)
cv2.waitKey(0)

```
![image](https://github.com/user-attachments/assets/aeb27eed-b7fa-4ef5-908b-ef5372953ac0)

#### Vertical:

```
flipped_vertically = cv2.flip(image, 0)

cv2.imshow('Flipped Vertically', flipped_vertically)
cv2.waitKey(0)
```

![image](https://github.com/user-attachments/assets/530e1822-9c51-4ce9-9a7f-19d96386b505)

### viii)Write and Save the Modified Image:

```
cv2.imwrite('modified_image.jpg', image)

cv2.destroyAllWindows()
```

![Screenshot 2024-09-16 084957](https://github.com/user-attachments/assets/2f525971-40ad-4e88-a25e-51350e9840a7)
![Screenshot 2024-09-16 085018](https://github.com/user-attachments/assets/9d65935d-090d-41e4-8218-814d6ae7a683)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







