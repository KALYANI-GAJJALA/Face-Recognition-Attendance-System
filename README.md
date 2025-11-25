### Face Recognition Attendance System

This project is a complete end-to-end Face Recognition Attendance System built using Python, OpenCV, MediaPipe FaceMesh, NumPy, Pandas, and scikit-learn. It supports real-time face registration, login, logout, and attendance tracking using a simple command-line interface.

Features Real-time Face Detection

Uses MediaPipe FaceMesh (**478** facial landmarks).

Highly accurate geometry-based facial embedding.

### Face Recognition Engine

Normalizes facial landmarks with reference points.

Generates a flattened feature vector of length **1434**.

Trains a Random Forest classifier on landmark embeddings.

Loads initial data from final_data.csv.

Registration

Detect a face and press S to start.

Captures **300** facial samples per user.

Saves the samples to the dataset.

Login

Detects face and press I to identify.

Predicts the user.

Records login time and assigns status (On-Time / Late Login).

Logout

Detects face and press O to confirm logout.

Predicts identity again.

Calculates working hours.

Saves entry into Attendance System.csv.

Command-Line Menu
## Register
2. Login
## Logout
4. Exit

### Tech Stack

Python 3

OpenCV

MediaPipe (FaceMesh model)

NumPy

Pandas

scikit-learn (RandomForestClassifier)

### How It Works

## Registration

Press S to capture facial samples.

Collects **300** frames of landmark data.

Normalizes embeddings and appends to the dataset.

2. Login

Press I to authenticate.

Predicts the user.

Records login timestamp and status.

## Logout

Press O to confirm logout.

Computes working hours automatically.

Saves information to Attendance System.csv.

### Project Structure

project/ │── face_attendance.py │── final_data.csv │── Attendance System.csv │── **README**.md │── requirements.txt

Installation ### Install Dependencies pip install -r requirements.txt

Run the Application python face_attendance.py

### Example Requirements File

opencv-python mediapipe pandas numpy scikit-learn
