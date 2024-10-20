# Gesture-Based Tool for Sterile Browsing of Radiology Images

This project implements a gesture-based interface for surgeons to browse through radiology images without physical contact, maintaining a sterile environment in the operating room.

## Features

- Hand gesture recognition for image navigation
- Touchless interface for maintaining sterility
- Image zooming, rotation, and navigation
- Web-based interface using Flask

## Requirements

- Python 3.10
- OpenCV (cv2)
- cvzone
- Flask

## Installation

1. Clone the repository
2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

## Usage

1. Run the Flask application:
   ```
   python app.py
   ```
2. Open a web browser and navigate to `http://localhost:5000`
3. Click on the "Start Application" button to launch the gesture-based interface

## Gesture Controls

- Index finger up: Zoom in
- Index and middle fingers up: Zoom out
- Index, middle, and ring fingers up: Go to last image
- Four fingers up (except thumb): Next image
- All fingers up: Previous image
- Thumb and little finger up: Go to first image
- Little and ring fingers up: Rotate clockwise
- Little, ring, and middle fingers up: Rotate counter-clockwise
- Index and little fingers up: Quit application

## File Structure

- `app.py`: Main application file
- `templates/`: HTML templates for web interface
- `static/`: Static files (CSS, images)
- `uploads/`: Directory for storing radiology images

## How it Works

1. The application uses OpenCV for image processing and hand detection.
2. cvzone's HandTrackingModule is used for hand gesture recognition.
3. Flask is used to create a web interface for launching the application.
4. The main logic is in the `application()` function, which handles gesture recognition and image manipulation.

## Note

Ensure that the radiology images are placed in the `uploads/` directory and named sequentially (1.jpg, 2.jpg, etc.).
