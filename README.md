# Attendance System Project README

## Project Overview

The Attendance System Project aims to build a comprehensive solution for tracking student attendance and detecting emotions using machine learning models. The system performs face recognition to identify students, detects their emotions, and logs attendance in a CSV file within a specific time window.

## Project Directory Structure

- `data/`
  - `students/`: Contains images of students organized in folders named after the student.
  - `emotions/`: Contains labeled emotion images organized in folders named after the emotion.

- `models/`
  - `face_recognition_model.h5`: The trained model for face recognition.
  - `emotion_detection_model.h5`: The trained model for emotion detection.

- `attendance.csv`: Logs attendance data including student names, detected emotions, and timestamps.

- `Attendance_System.ipynb`: Jupyter Notebook containing code for training the face recognition and emotion detection models.

- `face_recognition.py`: Python script for loading the face recognition model and identifying students.

- `emotion_detection.py`: Python script for loading the emotion detection model and identifying emotions.

- `attendance_system.py`: Main script to integrate face recognition, emotion detection, and attendance logging.

- `requirements.txt`: List of Python dependencies needed for the project.

- `README.md`: Documentation for the project.

## Getting Started

To get started with the project, follow these steps:

### Clone the Repository

Clone the project repository to your local machine using:

```bash
git clone <repository-url>

### Install Dependencies

Navigate to the project directory and install the required Python packages using:

```bash
pip install -r requirements.txt

### Prepare Data

- Place student face images in `data/students/` with folders named after each student.
- Place emotion images in `data/emotions/` with folders named after each emotion.

### Train Models

Open the `Attendance_System.ipynb` notebook and execute the cells to train both the face recognition and emotion detection models. Ensure that the models are saved in the `models/` directory.

### Run the Attendance System

- Place the image files you want to test in the appropriate location.
- Run the `attendance_system.py` script to start marking attendance. Ensure the script checks for the correct time window (e.g., 9:30 AM to 10:00 AM).

### Check Logs

The `attendance.csv` file will be updated with the student names, detected emotions, confidence levels, and timestamps.

### Scripts Overview

- **Attendance_System.ipynb**: Contains code for preprocessing data, training models, and saving them. It includes training for both face recognition and emotion detection models.

- **face_recognition.py**: Loads the face recognition model and provides functionality to recognize faces from images. It outputs the student ID and confidence level.

- **emotion_detection.py**: Loads the emotion detection model and provides functionality to detect emotions from images. It outputs the emotion ID and confidence level.

- **attendance_system.py**: Integrates the face recognition and emotion detection models. It checks the time window and logs attendance details into `attendance.csv`.

### Dependencies

The project relies on the following Python packages:

- `tensorflow`: For building and training machine learning models.
- `opencv-python`: For image processing.
- `numpy`: For numerical operations.
- `scikit-learn`: For machine learning utilities and metrics.

### Usage

- **Training Models**: Execute the Jupyter Notebook `Attendance_System.ipynb` to train and save models.
- **Attendance Marking**: Run the `attendance_system.py` script to process images and log attendance. The system will only operate within the specified time window.

### Troubleshooting

- Ensure all dependencies are installed correctly.
- Verify that the directory structure matches the expected format.
- Check that image paths and folder names are correctly specified.
