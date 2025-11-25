# Face Recognition Attendance System

This project is a complete end-to-end Face Recognition Attendance System built using Python, OpenCV, MediaPipe FaceMesh, NumPy, Pandas, and scikit-learn.
It supports real-time face registration, login, logout, and attendance tracking using a simple command-line interface.

---
**Features**
- Real-time Face Detection
- Uses MediaPipe FaceMesh (478 facial landmarks)
- High accuracy and stable detection under different lighting conditions

**Face Recognition**
- Normalizes facial landmarks with reference reference points
- Generates a flattened embedding vector of length 1434
- Uses Random Forest Classifier for identity prediction
- Loads initial trained data from final_data.csv

**Registration**
- Detect a face and press S
- Captures 300 samples per user
- Generates landmarks and saves them into the dataset
- Automatically updates the model with new data

**Login**
- Detect a face and press I
- Predicts user identity
- Records login timestamp
- Assigns login status (On-Time / Late Login)

**Logout**
- Detect a face and press O
- Recognizes the user again
- Records logout time
- Calculates total work duration
- Saves final entry into Attendance System.csv

**Command-Line Menu**
1. Register
2. Login
3. Logout
4. Exit

**Tech Stack**
- Python 3
- OpenCV
- MediaPipe FaceMesh
- NumPy
- Pandas
- scikit-learn (RandomForestClassifier)
  
### How It Works
1. **Registration**
- Press S to start capturing samples
- Collects 300 frames per user
- Extracts FaceMesh landmarks
- Normalizes and appends embeddings to final_data.csv

2. **Login**
- Press I to authenticate
- Predicts user from embeddings
- Saves login timestamp

3. **Logout**
- Press O to logout
- Identifies the user
- Calculates work duration
- Saves complete attendance record into Attendance System.csv

**Project Structure**
project/
│── face_attendance.ipynb
│── final_data.csv
│── Attendance System.csv
│── README.md
│── requirements.txt

**Installation**
*Install Dependencies*
``` pip install -r requirements.txt ```

**Run the Application**
python face_attendance.py
