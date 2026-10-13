Hand Gesture Recognition System

A real-time hand gesture recognition application built using Python, PyTorch, OpenCV, and deep learning. The system uses a custom-trained Convolutional Neural Network (CNN) to classify hand gestures captured through a laptop webcam.

Features

- Real-time webcam-based gesture recognition
- Custom image dataset and CNN model
- Confidence-based gesture predictions
- Training and validation performance tracking
- Classification report and confusion matrix
- Modular, reproducible Python project structure

Supported Gestures

1. Open Palm
2. Fist
3. Victory
4. Thumbs Up
5. Pointing
6. OK Sign

Tech Stack

- Python 3.11
- PyTorch
- OpenCV
- NumPy
- scikit-learn
- Matplotlib
- Pillow

Project Structure

hand-gesture-recognition/
├── data/
│   └── raw/
├── models/
├── reports/
├── src/
│   ├── __init__.py
│   ├── model.py
│   ├── collect_data.py
│   ├── train_model.py
│   └── predict_webcam.py
├── requirements.txt
├── .gitignore
└── README.md

Installation

Clone the repository:

git clone YOUR_REPOSITORY_URL
cd hand-gesture-recognition

Create a virtual environment:

py -3.11 -m venv .venv

Activate it on Windows:

.\.venv\Scripts\Activate.ps1

Install dependencies:

python -m pip install -r requirements.txt

Usage

1. Collect a custom dataset

python -m src.collect_data --label open_palm

Repeat for all six gesture classes. Press "SPACE" to save an image and "Q" to exit.

2. Train the model

python -m src.train_model

The trained model and evaluation reports will be saved in the "models/" and "reports/" directories.

3. Run live recognition

python -m src.predict_webcam

Press "Q" to close the webcam window.

Model Evaluation

Evaluate the model using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Training and validation curves

Actual evaluation results will be added after training and testing.

Limitations

The initial implementation classifies an image crop from a fixed webcam region. It does not independently detect hand presence, so unfamiliar objects and empty backgrounds may produce incorrect predictions.

Future Enhancements

- Hand detection and background rejection
- More gesture classes
- Transfer learning with MobileNetV3 or ResNet18
- Gesture-controlled applications
- Real-time inference optimization
- Improved generalization across users and environments

License

Choose an appropriate open-source license before distributing the project.

---

Project status: Initial development and custom dataset collection.
