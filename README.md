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
img = cv2.imread('1.png')
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
import cv2
img = cv2.imread("1.png")
img1= cv2.resize(img, (270,190))
#converting  bgr to hsv so it can be converted into rgb and bgr
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
hsv_rgb = cv2.cvtColor(hsv, cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB", hsv_rgb)
hsv_bgr = cv2.cvtColor(hsv, cv2.COLOR_HSV2BGR)
cv2.imshow("HSV2BGR", hsv_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# iii)Convert RGB and BGR to YCrCb
```python
import cv2
img = cv2.imread("1.png")
img1= cv2.resize(img, (270,190))
cv2.imshow("BGR_COLOR ", img1)
img_ycrcb = cv2.cvtColor(img1 , cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR2YCRCB ", img_ycrcb)
#converting  rgb to bgr so it can be converted into YCrCb
img_bgr = cv2.cvtColor(img1, cv2.COLOR_BGR2RGB)
cv2.imshow("RGB COLOR", img_bgr)
img_bgr_y = cv2.cvtColor(img_bgr, cv2.COLOR_BGR2YCrCb)
cv2.imshow("RGB2YCrCb", img_bgr_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# iv)Split and Merge RGB Image
```python
import cv2
img = cv2.imread("1.png")
img1= cv2.resize(img, (270,190))
#converting  bgr to hsv so it can be converted into rgb and bgr
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
h,s,v = cv2.split(hsv)
cv2.imshow("HUE IMAGE", h)
cv2.imshow("SATURATION IMAGE", s)
cv2.imshow("GRAY IMAGE", v)
#Merge:
mergered_HSV = cv2.merge([h,s,v])
cv2.imshow("MERGED HSV IMAGE", mergered_HSV)
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
<img width="407" alt="image" src="https://user-images.githubusercontent.com/93427183/228283690-170111dc-58ea-4820-bea3-a8d43a9ac572.png">


### iii) RGB and BGR to YCrCb
<img width="434" alt="image" src="https://user-images.githubusercontent.com/93427183/228285529-7a5cb0d3-6a8e-4213-887f-5604cb74ed74.png">

### iv) Split and merge RGB Image
<img width="418" alt="image" src="https://user-images.githubusercontent.com/93427183/228286313-6afdbbe8-f0f3-43f4-bbde-e40f36a19e42.png">


### v) Split and merge HSV Image
<img width="409" alt="image" src="https://user-images.githubusercontent.com/93427183/228287320-93142dd4-d22b-4c50-bfd2-e5cccf3e738d.png">



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
