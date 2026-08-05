# Child Safety Monitoring System

A real-time child safety monitoring application that uses computer vision to detect facial emotions and identify potentially dangerous situations. The system provides live webcam monitoring and can send emergency SMS alerts to guardians using Twilio.

---

## Features

- 👶 Real-time child monitoring
- 😊 Facial emotion recognition
- ⚠️ Danger detection
- 📹 Live webcam monitoring
- 📱 SMS emergency alerts using Twilio
- 🌐 Flask-based web application
- 🚨 Real-time safety notifications

---

## Tech Stack

### Frontend
- HTML5
- CSS3
- JavaScript

### Backend
- Python
- Flask

### Computer Vision & AI
- OpenCV
- YOLOv8
- TensorFlow / Keras

### APIs & Services
- Twilio SMS API

### Tools
- Git
- GitHub
- Docker

---

## Project Structure

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

## Installation

### Clone the repository

```bash
git clone https://github.com/BommenaDeepika/child-safety-monitoring-system-project.git
```

### Navigate to the project

```bash
cd child-safety-monitor
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run the application

```bash
python app.py
```

Open your browser and visit:

```
http://127.0.0.1:5000
```

---

## Docker

Build the Docker image

```bash
docker build -t child-safety-monitor .
```

Run the container

```bash
docker run --rm -p 5000:5000 child-safety-monitor
```

---

## Configuration

If you want to enable SMS alerts, configure the following environment variables:

- TWILIO_ACCOUNT_SID
- TWILIO_AUTH_TOKEN
- TWILIO_PHONE_NUMBER
- RECIPIENT_PHONE_NUMBER



---

## Future Enhancements

- Mobile application
- GPS tracking integration
- Cloud deployment
- Parent dashboard
- Email notifications
- Improved object and activity detection

---

## Author

**Deepika Bommena**

Bachelor of Technology (Computer Science Engineering)

---

## License

This project is developed for educational and academic purposes.
