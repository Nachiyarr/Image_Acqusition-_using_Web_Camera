# Image_Acqusition-_using_Web_Camera
## Aim
 To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import the cv2 and numpy package.
### Step 2:
Read the Video frame using the cv2.VideoCapture(0)
### Step 3:
Write the image using imwrite().
### Step 4:
Display the frame using the imshow().
### Step 5:
Divide the frame into halves and assign the smaller frame


## Program:
### Developed By:Alagu nachiyar k
### Register No:212222240006

## i) Write the frame as JPG file
```
import cv2
cap = cv2.VideoCapture(0)
frame_number = 0 # Initialize frame number
while frame_number < 5:
    ret, frame = cap.read()
    cv2.imshow('frame', frame)
    cv2.imwrite(f"frame_{frame_number}.jpg", frame)
    frame_number += 1
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
        cap.release()
        cv2.destroyAllWindows()
# Note: Press 'q' on your keyboard to stop recording from the webcam

```
## ii) Display the video
```
import cv2
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
        cap.release()
        cv2.destroyAllWindows()

```
## iii) Display the video by resizing the window
```
import cv2
cap = cv2.VideoCapture(0)
# Create a resizable window
cv2.namedWindow('Video', cv2.WINDOW_NORMAL)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    cv2.resizeWindow('Video', 100, 200)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
        cap.release()
        cv2.destroyAllWindows()


```
## iv) Rotate and display the video
```
import cv2
cap = cv2.VideoCapture(0)
# Define the rotation angle (in degrees)
rotation_angle = 90
while True:
    ret, frame = cap.read()
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    cv2.imshow('Rotated Video', rotated_frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
        cap.release()
        cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
![image](https://github.com/Nachiyarr/Image_Acqusition-_using_Web_Camera/assets/113497340/3d11e716-7055-434b-9f7c-5d0f73959aa9)

### ii) Display the video
![image](https://github.com/Nachiyarr/Image_Acqusition-_using_Web_Camera/assets/113497340/3d11e716-7055-434b-9f7c-5d0f73959aa9)


### iii) Display the video by resizing the window
![Screenshot 2024-05-07 182022](https://github.com/Nachiyarr/Image_Acqusition-_using_Web_Camera/assets/113497340/6ff05ba2-38e9-4b8d-97d1-d9d34b3188cc)

### iv) Rotate and display the video
![Screenshot 2024-05-07 182330](https://github.com/Nachiyarr/Image_Acqusition-_using_Web_Camera/assets/113497340/7e08e184-b339-46ad-8fb2-7b3af2213442)

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
