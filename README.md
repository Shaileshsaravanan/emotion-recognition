# Emotion Recognition

This project is an emotion recognition system that uses a Convolutional Neural Network (CNN) to detect and classify human emotions from real-time video streams. The model is trained using facial expressions and can classify emotions into seven categories: Angry, Disgust, Scared, Happy, Sad, Surprised, and Neutral.

![Emotion Recognition Demo](emotion_recognition_demo.gif)

## Repository Structure

```
emotion-recognition/
│
├── main/
│   ├── haarcascade_files/
│   │   └── haarcascade_frontalface_default.xml
│   ├── final.hdf5
│   ├── emotion_recognition.py
│   └── requirements.txt
│
├── train/
│   └── # Training data and scripts
│
└── test/
    └── # Testing data and scripts
```

- **main/**: Contains the necessary files to run the emotion recognition system.
  - **haarcascade_files/**: Contains the Haar cascade XML file for face detection.
  - **final.hdf5**: The trained model file.
  - **emotion_recognition.py**: The main script to run the emotion recognition system.
  - **requirements.txt**: Lists all the dependencies required to run the project.
- **train/**: Contains data and scripts used for training the model.
- **test/**: Contains data and scripts used for testing the model.

## Installation

### Prerequisites

Ensure that you have Python 3.7 or above installed on your system. You'll also need `pip` for installing the necessary Python packages.

### Clone the Repository

```bash
git clone https://github.com/shaileshsaravanan/emotion-recognition.git
cd emotion-recognition/main
```

### Install Dependencies

Install the required Python packages using `requirements.txt`:

```bash
pip install -r requirements.txt
```

## Running the Emotion Recognition System

Once all dependencies are installed, you can run the emotion recognition system using the following command:

```bash
python emotion_recognition.py
```

This will start the webcam feed, and the system will begin detecting faces and classifying emotions in real-time. The classified emotion and its probability will be displayed directly on the video stream.

### How It Works

1. **Face Detection**: The system uses the Haar cascade classifier (`haarcascade_frontalface_default.xml`) to detect faces in the video feed.
2. **Preprocessing**: The detected face region is converted to grayscale, resized to 64x64 pixels, and normalized.
3. **Emotion Classification**: The preprocessed face region is passed to the CNN model (`final.hdf5`), which predicts the probabilities for each of the seven emotions.
4. **Display Results**: The system displays the detected emotion with the highest probability on the video stream along with a horizontal bar indicating the strength of each emotion.

### Exiting the Program

To stop the program, press the `q` key.

## Acknowledgments

This project is based on the concepts of computer vision and deep learning, specifically in the domain of emotion recognition using facial expressions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
