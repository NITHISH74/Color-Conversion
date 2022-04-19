# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import CV2 library.
### Step2:
Use cv2.cvtcolor() to convert colot in required image.
### Step3:
Use .imshow() to display and .imwrite() to save.

### Step4:
Use split() to disperse color into separate channels.


### Step5:
Use merge() to combine those separate channels into color.


## Program:

```
# Developed By: NITHISHWAR S
# Register Number:212221230071
# i) Convert BGR and RGB to HSV and GRAY

import cv2
BGR_image=cv2.imread('12.png')
cv2.imshow('BGR_Image',BGR_image)
#BGR2HSV
hsv_image=cv2.cvtColor(BGR_image,cv2.COLOR_BGR2HSV)
cv2.imshow('212221230093',hsv_image)
cv2.imwrite('hsv.jpg',hsv_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

import cv2
HSV_image=cv2.imread('12.png')
cv2.imshow('HSV_Image',HSV_image)
#HSV2BGR
bgr_image=cv2.cvtColor(HSV_image,cv2.COLOR_HSV2BGR)
cv2.imshow('212221230093',bgr_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
BGR_image=cv2.imread('12.png')
cv2.imshow('BGR_Image',BGR_image)
#BGR2YCrCb
YCrCb_image=cv2.cvtColor(BGR_image,cv2.COLOR_BGR2YCrCb)
cv2.imshow('212221230093',YCrCb_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
BGR_image=cv2.imread('12.png')
blue=BGR_image[:,:,0]
green=BGR_image[:,:,1]
red=BGR_image[:,:,2]
cv2.imshow('BGR_Blue',blue)
cv2.imshow('BGR_Green',green)
cv2.imshow('BGR_Red',red)
merge_bgr=cv2.merge((blue,green,red))
cv2.imshow('merge_bgr',merge_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image

import cv2
house_color_image=cv2.imread('hsv.jpg')
h, s, v = cv2.split(house_color_image)
cv2.imshow('h',h)
cv2.imshow('s',s)
cv2.imshow('v',v)
merge_hsv=cv2.merge((h,s,v))
cv2.imshow('merge_hsv',merge_hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Output:
### i) BGR and RGB to HSV and GRAY

![image](https://user-images.githubusercontent.com/94164665/163960162-b1bee9d0-6db1-40b9-b721-33a2dc02702c.png)

### ii) HSV to RGB and BGR
![image](https://user-images.githubusercontent.com/94164665/163960217-52bfc727-b364-4c64-baa3-48d77773fff5.png)

### iii) RGB and BGR to YCrCb
![image](https://user-images.githubusercontent.com/94164665/163960276-8cc8b93e-83b3-4ab3-aa09-5a47c4a5f320.png)


### iv) Split and merge RGB Image
![image](https://user-images.githubusercontent.com/94164665/163960414-aff2323e-6c0d-4865-b10e-1e41f70118fa.png)


### v) Split and merge HSV Image

![image](https://user-images.githubusercontent.com/94164665/163960961-f321e3e5-cf5d-4b58-926b-91e9980deb6d.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
