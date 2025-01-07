# Pose Detector System

This repository contains a Pose Detector System that uses OpenCV and MediaPipe to detect human poses in images and real-time video streams. The system leverages machine learning models provided by MediaPipe to identify pose landmarks and visualize them on the input.

## Features

- **Real-time Pose Detection:** Detects human poses in video streams from a webcam.
- **Image Processing:** Performs pose detection on static images.
- **3D Landmark Visualization:** Visualizes pose landmarks in a 3D space.
- **FPS Display:** Displays the frame rate for real-time pose detection.
- **Flexible Output:** Allows for annotations on images and video frames.

---

## Prerequisites

Ensure you have Python installed along with the required libraries:

- OpenCV
- MediaPipe
- Matplotlib
- NumPy

Install the dependencies using:
```bash
pip install opencv-python mediapipe matplotlib numpy
```

---

## Usage

### 1. Pose Detection on Static Images

The `detectPose` function processes static images to detect pose landmarks and annotate them. To use it:

1. Provide the path to an image.
2. Call the `detectPose` function.

Example:
```python
image = cv2.imread('path_to_image.jpg')
detectPose(image, pose, display=True)
```

### 2. Real-time Pose Detection

Real-time pose detection is implemented using a webcam. To run it:

1. Ensure a webcam is connected.
2. Execute the script and allow camera access.

Press `q` to exit the video stream.

Example:
```python
python pose_detector.py
```

---

## Workflow

1. **Image Preparation:**
   - Convert input images from BGR to RGB for MediaPipe processing.

2. **Pose Detection:**
   - Detect human pose landmarks using MediaPipe.

3. **Visualization:**
   - Annotate the detected pose landmarks on the image or video frame.
   - Display 3D pose landmarks (for static images).

4. **Performance Measurement:**
   - Calculate and display FPS for real-time video processing.

---

## Results

The system accurately detects human poses in various scenarios and displays annotated images or video frames with pose landmarks.

### Example Output:

- **Static Image Pose Detection:**
  ![Static Pose Detection Example](example_static.png)

- **Real-time Video Pose Detection:**
  ![Real-time Pose Detection Example](example_realtime.gif)

