# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image.

### Step2:
Read the saved image using cv2.imread("filename.jpg").

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) 
and similarly for other color formats. 

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v]) 

### Step5:
Output the image using cv2.imshow("OUTPUT", image)


## Program:

### Developed By: U.SRINIVAS
### Register Number: 212221230108

# i) Convert BGR and RGB to HSV and GRAY
```python
import cv2
img = cv2.imread('asta.jpg')
cv2.imshow('original',img)

bgr2hsv = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR To HSV',bgr2hsv)

bgr2gray = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR To GRAY',bgr2gray)

rgb2hsv = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',rgb2hsv)

rgb2gray = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',rgb2gray)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

# ii)Convert HSV to RGB and BGR
```python
cv2.imshow('HSV',bgr2hsv)

hsv2rgb = cv2.cvtColor(bgr2hsv,cv2.COLOR_HSV2RGB)
cv2.imshow('HSVtoRGB',hsv2rgb)

hsv2bgr = cv2.cvtColor(bgr2hsv,cv2.COLOR_HSV2BGR)
cv2.imshow('HSVtoBGR',hsv2bgr)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

# iii)Convert RGB and BGR to YCrCb
```python
cv2.imshow('RGB',img_rgb)

rgb2YcrCb = cv2.cvtColor(img_rgb,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGBtoYCrCb',rgb2YcrCb)

bgr2YcrCb = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('BGRtoYCrCb',bgr2YcrCb)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

# iv)Split and Merge RGB Image
```python
b,g,r = cv2.split(img)
cv2.imshow("RED MODEL", r)
cv2.imshow("GREEN MODEL", g)
cv2.imshow("BLUE MODEL ", b)

merger = cv2.merge([b,g,r])
cv2.imshow("MERGED IMAGE", merger)

cv2.waitKey(0)
cv2.destroyAllWindows()
```



# v) Split and merge HSV Image
```python
cv2.imshow("INITIAL_HSV ", bgr2hsv)

h,s,v = cv2.split(bgr2hsv)
cv2.imshow("RED MODEL", h)
cv2.imshow("GREEN MODEL", s)
cv2.imshow("BLUE MODEL ", v)

merger = cv2.merge([h,s,v])
cv2.imshow("MERGED IMAGE", merger)

cv2.waitKey(0)
cv2.destroyAllWindows()
```



## Output:
### i) BGR and RGB to HSV and GRAY
<img width="545" alt="image" src="https://user-images.githubusercontent.com/93427183/228265835-0e48df0f-d18d-40c4-b838-2cc4fb1e78af.png">

<img width="1067" alt="image" src="https://user-images.githubusercontent.com/93427183/228267507-f9e828c8-9c1a-4174-aec7-f5c139f9e5c6.png">

### ii) HSV to RGB and BGR
![output](ss4.png)

![output](ss5.png)

![output](ss6.png)

### iii) RGB and BGR to YCrCb
![output](ss7.png)

![output](ss8.png)
### iv) Split and merge RGB Image
![output](ss9.png)

![output](ss10.png)

![output](ss11.png)

![output](ss12.png)

### v) Split and merge HSV Image
![output](ss13.png)

![output](ss14.png)

![output](ss15.png)

![output](ss16.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
