# Virtual-AI-Volume-Controller

This project lets you control the volume of the respective system by hand gestures. 
It captures your live video via webcam; on basis of 
which it detects hand gestures, locates the landmarks and calculates the distance
between the thumb and index finger and displays the same(pictorially) along with FPS (Frames Per Seconds).
The result of the detection lets the volume to be controlled via the calculated distance. furthermore, By changing gestures one can change the volume, giving flexibility as there's no contact involves.

## Installation
OS: Garuda Linux \
Platform: python3 
```bash
  sudo pacman -Syu  #update
  sudo pacman install python3
```
Library: OpenCv, mediapipe, Numpy
```bash
  sudo pacman -S python-pip
  python3 -m pip install opencv-python
  python3 -m pip install mediapipe
  python3 -m pip show numpy
```
## Screenshots

![App Screenshot](img.png)
## How to run it

- run it in ide of your choice (preferred on vscode)

- Once the code gets executed, it will automatically start detecting

- press `ESC` to quit the execution

## Process

### Capture original image

Live video will get captured using webcam:

```python
cap = cv2.VideoCapture(0)
```

### Gesture Detector

G gesture gets detected using `handTracking_module.py`

class: `hand_detector`

`__intit__()` : All the self variables are declared
 and initialized to the aruments passed
  (if not passed then to a pre-denined value) 
  which will be needed to locate the landmarks and 
  illustrate that on the video captured.

`findPose()` :Takes up each frame of the captured video and gray scale it 
and processes the resultant frame. Returns the processed image. 

![App Screenshot](img.jpg)

`findPosition()` :Takes the image(i.e. frame) and locates landmarks at different parts of hands(specified in mediapipe). Returns list of all the landmarks' Positions.

![App Screenshot](img.jpg)

mediapipe landmarks

![App Screenshot](img.jpg)

## Run Locally

Clone the project

```bash
  git clone https://github.com/TanishkaKumari/Virtual-AI-Volume-Controller
```

Go to the project directory

```bash
  cd gesture_volume_controller
```

Install dependencies

Start the server

```bash
  npm run start
```
