# License Plate Detection Project

This repository contains code for a license plate detection project. The project utilizes object detection models to identify vehicles and their corresponding license plates in video footage. The code is written in Python and employs various computer vision techniques and libraries.

## Technologies Used

- [ultralytics YOLO](https://github.com/ultralytics/yolov5): A popular object detection framework used for detecting vehicles and license plates in video frames.
  
- [roboflow](https://roboflow.com/): A platform for managing and deploying computer vision models. It's used here for loading a license plate detection model.

- [EasyOCR](https://github.com/JaidedAI/EasyOCR): A deep learning-based optical character recognition (OCR) library, used for reading license plate text.

- [OpenCV](https://opencv.org/): A powerful computer vision library used for image and video processing tasks.

- [SORT (Simple Online and Realtime Tracking)](https://github.com/abewley/sort): A tracking algorithm used for tracking vehicles in video frames.

## How It Works

1. The project uses Ultralytics YOLO to detect vehicles in each video frame.

2. The detected vehicle bounding boxes are tracked across frames using the SORT algorithm.

3. Ultralytics YOLO is also used to detect license plates within the video frames.

4. License plates are cropped and processed to extract the license plate number.

5. EasyOCR is employed to read the license plate number from the cropped license plate image.

6. The results, including the vehicle's bounding box, the license plate's bounding box, text, and scores, are stored in a dictionary for each frame.

7. The final results are written to a CSV file for further analysis.

## How to Use

1. **Clone this repository:**

    ```bash
    git clone https://github.com/SyaugiAlkaf/platedetection-syaugi.git
    cd platedetection-syaugi
    ```

2. **Install the required dependencies using `pip` & Run the main training script:**

    ```bash
    pip install ultralytics opencv-python-headless sort easyocr
    python main.py
    ```

3. **Observe the training progress and the rewards plot that visualizes the agent's learning.**

## Note

- This project demonstrates the integration of object detection, tracking, and optical character recognition for license plate detection in video. The code may need adjustments to work with your specific use case or models.

- Feel free to contribute, experiment, and improve upon the code!
   
