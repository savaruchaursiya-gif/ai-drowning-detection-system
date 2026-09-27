# 🏊 AI Drowning Detection System

An AI-powered swimming pool safety monitoring system that uses **YOLOv8, OpenCV, NumPy, and Streamlit** to detect people in video footage and identify prolonged periods of minimal movement that may indicate a potential drowning situation.

## 📌 Overview

Drowning incidents can occur quickly and may not always be noticed immediately by human observers. This project explores the use of **Computer Vision and Artificial Intelligence** to assist in monitoring swimming-pool environments.

The system processes video frames, detects people using **YOLOv8**, tracks their detected positions, and analyzes movement over time. When a person shows very little movement for a predefined period, the system displays a **DROWNING ALERT** on the video stream.

> **Note:** This is an academic/prototype project and should not be considered a certified life-safety or emergency-response system.

## ✨ Features

* 👤 Real-time person detection using **YOLOv8**
* 🎥 Upload and process pre-recorded swimming-pool videos
* 📷 Live camera monitoring
* 📊 Movement-based activity analysis
* 🚨 Automatic potential drowning alert
* 🖥️ Interactive web interface using **Streamlit**
* ⚡ Frame-by-frame video processing using **OpenCV**
* 🔍 Visual bounding boxes around detected people

## 🧠 How It Works

The system follows these main steps:

```text
Video / Live Camera
        ↓
   Read Video Frame
        ↓
      YOLOv8
        ↓
   Detect Persons
        ↓
Calculate Person Position
        ↓
 Compare Movement
        ↓
Low Movement for
Predefined Duration
        ↓
  Potential Drowning
        ↓
   🚨 Alert Display
```

### Detection Logic

1. The video source is opened using OpenCV.
2. Each frame is passed to the YOLOv8 model.
3. The system identifies objects belonging to the **person** class.
4. Bounding boxes are drawn around detected people.
5. The center point of each detected person is calculated.
6. The current center point is compared with the previous position.
7. If movement remains below a predefined threshold for several seconds, the system displays a **DROWNING ALERT**.

## 🛠️ Technologies Used

| Technology    | Purpose                                 |
| ------------- | --------------------------------------- |
| **Python**    | Core programming language               |
| **YOLOv8**    | Person/object detection                 |
| **OpenCV**    | Video processing and frame manipulation |
| **NumPy**     | Numerical and movement calculations     |
| **Streamlit** | Web-based user interface                |

## 📂 Project Structure

```text
ai-drowning-detection-system/
│
├── app.py
├── requirements.txt
├── README.md
├── yolov8n.pt
└── sample_videos/
```

> The exact structure may vary depending on how you organize your project.

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/ai-drowning-detection-system.git
```

```bash
cd ai-drowning-detection-system
```

### 2. Create a virtual environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## 📦 Requirements

Create a `requirements.txt` file containing:

```text
streamlit
opencv-python
numpy
ultralytics
```

## 🚀 Running the Application

Start the Streamlit application using:

```bash
streamlit run app.py
```

The application will open in your browser.

You can then choose between:

### 🎥 Upload Video

Upload a swimming-pool video in one of the supported formats:

* `.mp4`
* `.avi`
* `.mov`

### 📷 Live Camera

Select **Live Camera** and start the camera to process the live video feed.

## 🖥️ Application Workflow

The application provides a simple interface where users can:

1. Select the video input source.
2. Upload a video or activate the camera.
3. Detect people in the video.
4. Monitor detected movement.
5. Receive an on-screen alert when prolonged minimal movement is detected.

## 🎯 Project Objective

The primary objective of this project is to demonstrate how **AI and Computer Vision can be applied to swimming-pool safety monitoring**.

The project provides practical experience with:

* Object detection
* Video processing
* Computer vision
* AI-based event detection
* Real-time monitoring
* Streamlit application development

## ⚠️ Limitations

The current prototype uses **movement analysis based on detected bounding-box center points**. Therefore, it may produce false positives or false negatives in situations such as:

* A person remaining still voluntarily
* Occlusion between people
* Rapid camera movement
* Poor lighting
* Reflections on the water
* Multiple people being close together
* Temporary YOLO detection loss
* Changes in camera angle

The system should therefore be considered a **prototype/research project**, not a replacement for trained lifeguards or certified safety equipment.

## 🔮 Future Improvements

Possible improvements include:

* 🔹 Persistent multi-object tracking using **YOLO tracking**
* 🔹 More robust person identification across frames
* 🔹 Pose estimation for detecting unusual body positions
* 🔹 Water-level and pool-region detection
* 🔹 Audio/siren notifications
* 🔹 Automatic emergency notification
* 🔹 Alert image/video recording
* 🔹 Improved temporal activity analysis
* 🔹 Custom-trained drowning detection model
* 🔹 Dashboard for monitoring multiple cameras
* 🔹 Cloud-based monitoring and alerting

## 📸 Screenshots

Add screenshots of your application here:

```text
screenshots/
├── dashboard.png
├── person-detection.png
└── drowning-alert.png
```

*VIDEO LINK:https://lnkd.in/p/dqipSk96

## 📚 Model

This project uses **YOLOv8 Nano (`yolov8n.pt`)** for object detection.

The model is used to identify people in the video stream. The drowning indication is then determined using the project's movement-analysis logic.

## 👨‍💻 Author

SAVARU CHAURSIYA..

* GitHub:https://github.com/savaruchaursiya-gif
* LinkedIn: www.linkedin.com/in/savaru-chaursiya-622721237

## 📄 License

This project is intended for **educational and research purposes**.



---

⭐ If you find this project interesting, consider giving the repository a star!
