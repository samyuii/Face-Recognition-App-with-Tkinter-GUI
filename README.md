---
title: Face Recognition App
description: A desktop application for face recognition using OpenCV and Tkinter.
---

# Face Recognition App

## Overview

The Face Recognition App is a desktop application designed to facilitate face recognition using OpenCV. This application allows users to collect face samples, train a face recognition model, and recognize faces based on the trained model. The user-friendly interface is built using Tkinter, and threading is utilized to keep the GUI responsive during long-running tasks such as sample collection, model training, and face recognition.

## Features

- **Sample Collection**: Collect face samples for a given name.
- **Model Training**: Train a face recognition model using the collected samples.
- **Face Recognition**: Recognize faces based on the trained model.
- **Tooltips**: Hover tips for each button to guide the user.

## Prerequisites

- Python 3.x
- OpenCV
- Numpy
- Tkinter

## Installation

1. **Clone the repository**:
   ~~~sh
   git clone https://github.com/yourusername/face-recognition-app.git
   cd face-recognition-app
   ~~~

2. **Install the required packages**:
   ~~~sh
   pip install -r requirements.txt
   ~~~

3. **Ensure OpenCV is installed**:
   ~~~sh
   pip install opencv-python opencv-contrib-python
   ~~~

## Usage

1. **Run the application**:
   ~~~sh
   python app.py
   ~~~

2. **Enter Your Name**:
   - Enter your name in the text box provided.

3. **Collect Samples**:
   - Click the "Collect Samples" button to start collecting face samples.
   - Ensure your face is visible in the webcam.
   - The process will collect 100 samples and save them to the specified directory.

4. **Train Model**:
   - Click the "Train Model" button to train the face recognition model with the collected samples.
   - Wait for the training process to complete.

5. **Recognize Faces**:
   - Click the "Recognize Faces" button to start face recognition.
   - Ensure your face is visible in the webcam.
   - The application will display the confidence level and recognize the face if it matches the trained model.

## Project Structure

- `app.py`: The main application script containing the GUI and the core functionality.
- `requirements.txt`: List of required packages.
- `image_samples/`: Directory where the collected face samples are stored.

## Functions

### `collect_face_samples(name, data_path)`

Collects face samples using the webcam and saves them to the specified directory.

- **Parameters**:
  - `name`: The name of the person whose samples are being collected.
  - `data_path`: The path to the directory where the samples will be saved.

### `train_face_recognition(data_path)`

Trains a face recognition model using the collected samples.

- **Parameters**:
  - `data_path`: The path to the directory where the samples are stored.

- **Returns**:
  - `model`: The trained face recognition model.

### `recognize_face(model, name)`

Recognizes faces using the trained model.

- **Parameters**:
  - `model`: The trained face recognition model.
  - `name`: The name of the person to be recognized.

## GUI Components

- **Labels**:
  - "Enter Your Name": Label for the name entry field.
  - Status Label: Displays the current status of the application.

- **Entry**:
  - Name Entry: Field for entering the user's name.

- **Buttons**:
  - "Collect Samples": Button to start sample collection.
  - "Train Model": Button to start model training.
  - "Recognize Faces": Button to start face recognition.

- **Tooltips**:
  - Hover tips for each button to guide the user.

## Threading

- **Threading** is used to keep the GUI responsive during long-running tasks such as sample collection, model training, and face recognition. Each of these tasks is run in a separate thread to avoid freezing the GUI.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes or enhancements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- This project uses the OpenCV library for computer vision tasks.
- Tkinter is used for the graphical user interface.

---

Feel free to customize this README to fit the specific details and requirements of your project.
~~~
