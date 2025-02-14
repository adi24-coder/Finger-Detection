
# Hand Gesture Recognition using OpenCV

This project implements a basic hand gesture recognition system using OpenCV and NumPy in Python. The program captures real-time video from the webcam, processes hand gestures, and identifies the number of fingers displayed.

## Features
- Captures video from the default webcam.
- Uses HSV color filtering to detect hand gestures.
- Applies morphological transformations for noise reduction.
- Detects the largest contour and convex hull of the hand.
- Identifies convexity defects to count fingers.
- Displays the number of fingers detected on the screen.
- Calculates and displays the FPS in real time.

## Prerequisites
Ensure you have the following dependencies installed before running the project:

```sh
pip install numpy opencv-python
```

## How to Run
1. Clone the repository:

   ```sh
   git clone https://github.com/your-username/hand-gesture-recognition.git
   cd hand-gesture-recognition
   ```

2. Run the script:

   ```sh
   python hand_gesture.py
   ```

3. The program will open a window displaying the camera feed with detected hand gestures.
4. Press `q` to exit the program.

## File Structure
```
hand-gesture-recognition/
│── hand_gesture.py    # Main script for hand gesture recognition
│── README.md          # Project documentation
```

## Explanation of Key Components
- **FPS Calculation**: The script calculates the frames per second (FPS) dynamically and displays it on the screen.
- **Hand Detection**: A sub-region of the frame (100x100 to 300x300) is analyzed to extract hand features.
- **HSV Thresholding**: Converts the cropped image to HSV and applies a binary mask to isolate skin color.
- **Morphological Transformations**: Uses dilation and erosion to refine the mask.
- **Contour Detection**: Identifies the largest hand contour and its convex hull.
- **Convexity Defects**: Uses defect points to determine the number of fingers raised.
- **Finger Counting**: Displays the corresponding number of fingers detected on the screen.

## Known Issues
- The accuracy of detection depends on proper lighting conditions.
- The HSV values may need to be adjusted for different skin tones.
- Works best against a plain background to avoid false positives.

## Future Improvements
- Integrating a deep learning model for improved accuracy.
- Implementing gesture-based commands for user interaction.
- Adding support for multiple hand tracking.

## License
This project is licensed under the MIT License. Feel free to modify and enhance it.

## Author
https://github.com/adi24-coder

