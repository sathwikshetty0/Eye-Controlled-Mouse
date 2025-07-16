Got it! Here’s the complete, nicely formatted **README.md** file with markdown, ready to use:

````markdown
# Eye Controlled Mouse

This project enables mouse control using eye movements detected from a webcam feed.
The program tracks eye landmarksusing **MediaPipe Face Mesh** and moves the mouse
pointer accordingly. It also detects blinking to perform mouse clicks.

---

## Features

- **Eye tracking**: Tracks the right eye position to move the mouse cursor on the screen.
- **Blink detection**: Detects blinking from the left eye to trigger mouse clicks.
- **Real-time**: Uses webcam feed for continuous eye movement detection.
- **Visual feedback**: Displays eye landmarks on the video feed for debugging.

---

## Requirements

- Python 3.7+
- OpenCV (`cv2`)
- MediaPipe
- PyAutoGUI
- math (standard Python library)

---

## Installation

1. Clone this repository or copy the script files.

2. Install dependencies using pip:

```bash
pip install opencv-python mediapipe pyautogui
````

---

## Usage

Run the script:

```bash
python eye_controlled_mouse.py
```

* The program will open your webcam and start tracking your eyes.
* Move your right eye to control the mouse pointer.
* Blink your left eye to perform a mouse click.
* Press `q` to quit the application.

---

## How It Works

1. **Face mesh detection**: The script uses MediaPipe’s Face Mesh to identify key facial landmarks.
2. **Mouse movement**: It tracks specific landmarks of the right eye to move the mouse pointer relative to your screen size.
3. **Blink detection**: It measures the vertical distance between two landmarks of the left eye to determine if the eye is closed (blinked).
4. **Click action**: When a blink is detected, a mouse click event is triggered via PyAutoGUI.

---

## Notes

* You might need to adjust the blinking threshold (`eye_open_distance < 5`) depending on your camera and lighting conditions.
* Make sure to run the program in a well-lit environment for better landmark detection.
* Use a laptop or external webcam with a clear frontal face view for optimal performance.
* The script flips the webcam feed horizontally to match natural movement.

---

## Troubleshooting

* If the mouse doesn’t move smoothly, try increasing the frame rate or using a higher-quality webcam.
* If blinking is not detected correctly, tweak the distance threshold or try a different eye landmark pair.
* PyAutoGUI may require additional permissions on some operating systems to control the mouse.
