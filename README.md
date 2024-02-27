# Image_Acqusition-_using_Web_Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image
<br>

### Step 3:
Use cv2.imwrite to save the image
<br>

### Step 4:
Use cv2.imshow to show the video
<br>

### Step 5:
End the program and close the output video window by pressing 'q'.
<br>

## Program:

### Developed By: Sathish R   
### Register No: 212222230138


## i) Write the frame as JPG file

```python
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("Sathish.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```


## ii) Display the video
```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('212222230138_Sathish',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```


## iii) Display the video by resizing the window


```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230138_Sathish',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```


## iv) Rotate and display the video


```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230138_Sathish',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
![Screenshot 2024-02-27 103108](https://github.com/r-sathish-02/Image_Acqusition-_using_Web_Camera/assets/118787261/7468fede-5d96-41e3-a291-091c9c0a60e4)

</br>
</br>


### ii) Display the video
![Screenshot 2024-02-27 103903](https://github.com/r-sathish-02/Image_Acqusition-_using_Web_Camera/assets/118787261/2ccfa47a-ed01-4720-9cd8-3a9d057f15bc)

</br>
</br>


### iii) Display the video by resizing the window
![Screenshot 2024-02-27 104015](https://github.com/r-sathish-02/Image_Acqusition-_using_Web_Camera/assets/118787261/998ae96e-0140-4b77-aca2-c12880be1c17)

</br>
</br>



### iv) Rotate and display the video
![Screenshot 2024-02-27 104211](https://github.com/r-sathish-02/Image_Acqusition-_using_Web_Camera/assets/118787261/ebe2f295-9f41-4780-8187-da5b5d5ff91a)

</br>
</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
