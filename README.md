# SafeStreets

**SafeStreets** is a mobile-connected computer vision-powered security camera system designed for real-time safety monitoring. Built at [HackTJ 12.0](https://hacktj.org/), the system detects physical violence and notifies users instantly while also allowing them to view and save footage from a connected camera.

The core goal is to enhance personal or residential security using machine learning models optimized for real-time performance and meaningful alerts.

---

## Features

### Real-Time Camera Integration
- **Connect to Camera:** SafeStreets connects to a physical USB webcam via OpenCV, serving as the live feed source.
- **Record Video:** Local video is recorded directly on the computer running the system.
- **Live Viewing on Phone:** Users can view the live feed from their phone through a connected Flutter mobile app.
- **Send Video to Phone:** Emergency footage and live feeds are streamed or sent to the mobile client.

### Detection & Alerting
- **Motion Detection:** Processing is only triggered when motion is detected, saving resources and reducing false positives.
- **Violence Detection:** Uses an LSTM-based model to detect fight-like motion when two or more people are present.
- **Real-Time Notifications:** When violence is detected, the system sends push notifications to the user immediately.

---

## Mobile App (Flutter)

The companion mobile app connects to the camera system over WiFi and offers:
- **Live Feed:** Watch the camera feed in real time.
- **Push Notifications:** Be instantly alerted to emergency events such as fights.
- **Video Playback:** Review recorded emergency event clips sent from the server.

---

## Built With

- Python (OpenCV, Flask, PyTorch)
- YOLOv8 for object/person detection
- LSTM for action recognition (violence detection)
- Flutter (mobile interface)
- Firebase Cloud Messaging (notifications)
