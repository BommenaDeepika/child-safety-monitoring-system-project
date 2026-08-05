# 🛡️ Child Safety Monitoring System

A real-time child safety monitoring application that uses computer vision to detect facial emotions and identify potentially dangerous situations. The system provides live webcam monitoring and can send emergency SMS alerts to guardians using Twilio.

---

# 📌 Overview

The Child Safety Monitoring System is designed to enhance child safety by combining computer vision and web technologies. It continuously monitors a live webcam feed, detects facial emotions, identifies dangerous situations, and sends emergency alerts when required.

This project is built using Python, Flask, OpenCV, TensorFlow, YOLOv8, HTML, CSS, and JavaScript.

---

# ✨ Features

- 👶 Real-time Child Monitoring
- 😊 Facial Emotion Recognition
- ⚠️ Danger Detection
- 📷 Live Webcam Monitoring
- 📱 SMS Emergency Alerts using Twilio
- 🌐 Flask-based Web Application
- 🚨 Real-time Safety Notifications

---

# 🛠️ Tech Stack

## Frontend
- HTML5
- CSS3
- JavaScript

## Backend
- Python
- Flask

## Computer Vision & AI
- OpenCV
- YOLOv8
- TensorFlow / Keras

## APIs & Services
- Twilio SMS API

## Tools
- Git
- GitHub
- Docker

---

# 📂 Project Structure

```
child-safety-monitor/
│── app.py
│── Test.py
│── templates/
│── static/
│── models/
│── requirements.txt
│── Dockerfile
│── README.md
```

---

# 🚀 Installation

## Clone the Repository

```bash
git clone https://github.com/BommenaDeepika/child-safety-monitoring-system-project.git
```

## Navigate to the Project Folder

```bash
cd child-safety-monitor
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

## Run the Application

```bash
python app.py
```

Open your browser and visit:

```
http://127.0.0.1:5000
```

---

# 🐳 Docker

## Build Docker Image

```bash
docker build -t child-safety-monitor .
```

## Run Docker Container

```bash
docker run --rm -p 5000:5000 child-safety-monitor
```

---

# ⚙️ Configuration

To enable SMS alerts, configure the following environment variables:

- TWILIO_ACCOUNT_SID
- TWILIO_AUTH_TOKEN
- TWILIO_PHONE_NUMBER
- RECIPIENT_PHONE_NUMBER

---

# 📸 Screenshots

Add screenshots of:

- Home Page
- Live Webcam Monitoring
- Emotion Detection
- Danger Detection
- SMS Alert
- Dashboard

---

# 🔮 Future Enhancements

- 📱 Mobile Application
- 📍 GPS Tracking Integration
- ☁️ Cloud Deployment
- 👨‍👩‍👧 Parent Dashboard
- 📧 Email Notifications
- 🤖 Improved Object & Activity Detection

---

# 👩‍💻 Author

**Deepika Bommena**

Bachelor of Technology (Computer Science Engineering)

---

# 📄 License

This project was developed for educational and academic purposes.
