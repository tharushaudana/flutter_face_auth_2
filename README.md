# Flutter Face Authentication 2

This is the updated version of the Flutter-based face authentication application. It detects faces using **Google ML Kit's face detection** and uses the **FaceNet512** model to recognize and differentiate users. Encoded face data is stored and retrieved from **Firebase Firestore**.

✅ Fully compatible with:
- **Flutter** 3.32.6 • channel stable • [flutter.git](https://github.com/flutter/flutter.git)  
- **Framework** revision 077b4a4ce1 (2025-07-08)  
- **Engine** revision 72f2b18bb0  
- **Dart** 3.8.1 • DevTools 2.45.1

---

## Features

- 👁️ **Face Detection with Google ML Kit**: Uses `google_mlkit_face_detection` to detect faces in real time.
- 🧠 **Face Encoding with FaceNet512**: Converts detected faces into 512-length feature vectors using the FaceNet512 model.
- ☁️ **Cloud Firestore Integration**: Stores and retrieves encoded face data (Float32 arrays) and associated names.
- 🔄 **Real-Time Face Authentication**: Predicts user identity by comparing current face data with stored vectors using cosine similarity.
- 📦 **On-device Inference with TFLite**: Utilizes `tflite_flutter` for running the FaceNet model locally on the device.

## Dependencies

```yaml
cupertino_icons: ^1.0.2
camera: ^0.10.5+5
google_mlkit_face_detection: ^0.13.1
image: ^3.0.2
tflite_flutter: ^0.11.0
cloud_firestore: ^4.13.2
firebase_core: ^2.23.0
````

## Screenshots

### App Interface

![App Interface](screenshots/01.jpg)

### Register New Face Page (when a face not in the database is detected)

![Predicted Page](screenshots/02.jpg)

### Predicted Page

![Data Storage in Firestore](screenshots/03.jpg)

### When a Face Is Not Detected Correctly

![When a Face Is Not Detected Correctly](screenshots/04.jpg)

### Data Storage in Firestore

![Data Storage in Firestore](screenshots/05.png)

## Getting Started

1. Clone this repository:

   ```bash
   git clone https://github.com/tharushaudana/flutter_face_auth_2.git
   cd flutter_face_auth_2
   ```

2. Install dependencies:

   ```bash
   flutter pub get
   ```

3. Set up Firebase for Android and iOS ([Firebase Setup Guide](https://firebase.google.com/docs/flutter/setup)).

4. Run the app:

   ```bash
   flutter run
   ```

## Purpose

This project demonstrates mobile face authentication using deep learning and real-time face detection. It is suitable for secure identity verification systems where user faces are encoded, stored, and compared efficiently using on-device AI and cloud storage.
