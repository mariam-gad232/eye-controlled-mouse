# eye-controlled-mouse
Real-time eye-gaze-controlled mouse interface using facial landmarks detection with MediaPipe.

## Features
- Real-time eye tracking using webcam
- Screen coordinate mapping for cursor control
- Blink detection for mouse clicks
- Smooth cursor movement with PyAutoGUI
- Facial landmark visualization

## Prerequisites
- Webcam
- Python 3.7+

## Installation
```bash
pip install opencv-python mediapipe pyautogui
```
## Usage
-run main.py

-Press 'q' to quit

-Ensure proper lighting conditions

-Position face within webcam frame

## How It Works
-Face Mesh Detection: Uses MediaPipe's 468-point facial landmark model
-Eye Tracking: Focuses on landmarks 474-477 (right eye contour)
-Cursor Mapping: Converts eye position to screen coordinates
-Click Detection: Measures vertical distance between landmarks 145-159 (left eye)
-PyAutoGUI for cross-platform input control

## Customization
-Adjust blink threshold: (left[0].y - left[1].y) < 0.004
-Modify screen scaling factors:
```bash
screen_x = int(x * screen_w / frame_w)
screen_y = int(y * screen_h / frame_h)
```



