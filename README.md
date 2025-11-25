# Face-Recognition-Attendance-System

A complete end-to-end **Face Recognition Attendance System** built using **Python, OpenCV, MediaPipe, scikit-learn, and Streamlit**. Designed with a clean **OOP-based architecture**, this application mimics real-world software design and provides a polished attendance management workflow.

---

## Features

### Real-time Face Detection

* Powered by **MediaPipe Face Mesh** with **468 facial landmarks**.
* Highly accurate geometry-based face representation.

### Face Recognition Engine

* Landmark normalization for consistent feature extraction.
* **Random Forest Classifier** used for face prediction.
* Model retrains **only when a new user is registered**.

### Login / Logout Workflow

* **Login Process:**

  * Webcam capture → Predict face → User confirmation → Log login time.
* **Logout Process:**

  * Recognize face → Save logout time → Auto-calculate work duration.

### Attendance Logging

All activity is stored in a single CSV file: `AttendanceSystem.csv` with:

* Name
* Login Time
* Login Status
* Logout Time
* Work Duration

### Clean Streamlit UI

* Live camera feed
* Register, Login, Logout buttons
* Clear on-screen messages
* Smooth user flow

### Modular OOP Architecture

Separate classes handle:

* Webcam & frame capture
* Facial landmark extraction
* Embedding generation
* Model training & storage
* Attendance CSV logging
* Streamlit front-end logic

---

## ️ Tech Stack

* **Python 3**
* **OpenCV** – Camera access & preprocessing
* **MediaPipe** – 468-point face mesh landmarks
* **scikit-learn** – Random Forest model
* **Streamlit** – UI layer
* **Pandas** – Data handling & CSV logging

---

## How It Works

### 1️⃣ Registration

* Capture **200 face samples** using webcam.
* Extract embeddings → Retrain & save recognition model.

### 2️⃣ Login

* Detect and identify the user.
* Ask for confirmation.
* Log login timestamp.

### 3️⃣ Logout

* Re-identify user.
* Log logout timestamp.
* Auto-compute **total working hours**.

---

## Project Structure (Example)

```
FaceRecognitionAttendanceSystem/
│── data/
│   ├── embeddings.pkl
│   ├── model.pkl
│   └── samples/
│
│── src/
│   ├── camera.py
│   ├── face_detector.py
│   ├── embedding_generator.py
│   ├── model_trainer.py
│   ├── attendance_logger.py
│   └── app.py
│
│── AttendanceSystem.csv
│── README.md
│── requirements.txt
```

---

## ▶️ Run the Application

### Install dependencies

```
pip install -r requirements.txt
```

### Start Streamlit app

```
streamlit run src/app.py
```

---

## Future Enhancements

* Add face recognition confidence scoring
* Integrate database instead of CSV
* Support for multiple cameras
* Admin dashboard with analytics

---

### ⭐ If you find this project useful, consider giving it a star on GitHub!
