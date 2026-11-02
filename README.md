# EXP-2-Record-Image-Acquisition-using-Web-Camera-SBKK
## Record-Image-Acquisition-using-Web-Camera-Completion-requirements

## Aim:

To write a Python program using OpenCV to capture an image from the webcam and perform the following operations:

* Write the frame as a JPG file
* Display the video
* Display the video by resizing the window
* Rotate and display the video

## Software Used:

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)

## Algorithm:

Step 1:
Import the required libraries and initialize the webcam using cv2.VideoCapture().

Step 2:
Capture frames continuously from the webcam.

Step 3:
Save a frame as a JPG image using cv2.imwrite().

Step 4:
Display the live video stream using cv2.imshow().

Step 5:
Resize the frame and rotate it using OpenCV functions, then display the processed frames.

## Program:

Developed By: SRIBALAKUMARAN R

Register No: 212225220104

## 1. Capture the image:
```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
```
```
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
```
```
captured_image = cv2.imread('captured_frame.jpg')
```
```
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()
```
## 2. Display the video:
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```

## 3. Display the video by resizing the window:
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

```

## 4. Rotate and display the video:

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```

## Output:

## 1. Capture the image:

<img width="625" height="431" alt="image" src="https://github.com/user-attachments/assets/0f281b2d-68e9-4355-bfc3-0a87bc92d4da" />


## 2. Display the video:

<img width="852" height="482" alt="image" src="https://github.com/user-attachments/assets/150a36e8-baf4-493c-b898-bf28b4efae83" />

## 3. Display the video by resizing the window:

<img width="528" height="487" alt="image" src="https://github.com/user-attachments/assets/39e0af88-d22d-461c-aa64-d59b8f60a362" />

## 4. Rotate and display the video:

<img width="635" height="677" alt="image" src="https://github.com/user-attachments/assets/099b9593-db33-48a3-8254-5585a2bdf2f8" />


## Result:
           
  Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.
