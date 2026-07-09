# ✍️ Air Drawing Alphabet Recognition System

A real-time machine learning application that recognizes handwritten uppercase English alphabets **A–Z** drawn in the air using index-finger movement captured through a webcam.

The system combines real-time hand tracking, computer vision, image preprocessing, and a tuned Random Forest classification pipeline. The final application is deployed using Streamlit Community Cloud.

## 🌐 Live Demo

Try the deployed application:

https://airdraw-alphabet-recognition.streamlit.app/

## 📌 Project Overview

The application allows users to draw uppercase English alphabets in real time without touching a physical surface.

The complete workflow is:

1. Capture live webcam frames
2. Detect and track the user's hand
3. Use index-finger movement for air drawing
4. Store the drawing on a virtual canvas
5. Detect the drawing region
6. Crop and center the alphabet
7. Resize the image to `34 × 34 × 3`
8. Apply preprocessing consistent with model input
9. Flatten the image into `3468` features
10. Predict the alphabet using the tuned Random Forest pipeline
11. Display the predicted class and confidence score

## ✨ Key Features

- Real-time webcam input
- MediaPipe-based hand tracking
- Index-finger air drawing
- Open-palm drawing clear gesture
- Virtual drawing canvas
- Automatic alphabet-region detection
- Bounding-box cropping
- Square centering
- `34 × 34 × 3` RGB model input
- Real-time A–Z classification
- Prediction confidence display
- Exact model-input visualization
- Streamlit web interface
- WebRTC browser camera integration
- Cloud deployment

## 🖼️ Application Screenshots

### 1. Live Application Interface

<img width="1918" height="906" alt="image" src="https://github.com/user-attachments/assets/dbad798a-82ac-4119-9582-ee5b5a4111b5" />


### 2. Real-Time Prediction — A
<img width="912" height="921" alt="Screenshot 2026-07-08 125408" src="https://github.com/user-attachments/assets/1c48e70c-c6ba-4495-b6ac-195b0465eeb5" />

### 3. Real-Time Prediction — B

<img width="630" height="925" alt="Screenshot 2026-07-08 125604" src="https://github.com/user-attachments/assets/c3fd28a1-7f2d-41b1-9286-a0d4bb2cdbee" />

### 4. Real-Time Prediction - C
<img width="683" height="917" alt="Screenshot 2026-07-08 125643" src="https://github.com/user-attachments/assets/591f75e6-354c-41be-a48c-7630534d8784" />

### 5. Real Time Prediction - X
<img width="720" height="928" alt="Screenshot 2026-07-08 131005" src="https://github.com/user-attachments/assets/ba478911-8ee3-4646-b8e4-172a0934392f" />


### 6. Real Time Prediction - Y
<img width="718" height="932" alt="Screenshot 2026-07-08 131147" src="https://github.com/user-attachments/assets/d64d4778-959b-4000-b22e-f73f296f8dc4" />

### 7. Real-Time Prediction — Z

<img width="732" height="940" alt="Screenshot 2026-07-08 131237" src="https://github.com/user-attachments/assets/fe176a8b-e30f-4f70-99fb-9f1095298cf5" />


## 🧠 Machine Learning Algorithms Evaluated

The following classification algorithms were evaluated during model development:

- K-Nearest Neighbors
- Naive Bayes
- Decision Tree
- Logistic Regression
- Linear SVM
- Random Forest

The final deployed model is a tuned Random Forest classification pipeline.

## 📊 Final Model Performance

The tuned Random Forest model achieved the following held-out test results:

| Metric | Score |
|---|---:|
| Accuracy | 85.59% |
| Precision | 85.91% |
| Recall | 85.59% |
| F1 Score | 85.54% |

These values correspond to the model-evaluation output obtained during project testing.

## 🔄 System Architecture

```text
Webcam Input
      ↓
MediaPipe Hand Detection
      ↓
Index Fingertip Tracking
      ↓
Air Drawing Canvas
      ↓
Drawing Region Detection
      ↓
Bounding Box Extraction
      ↓
Square Centering
      ↓
Resize to 34 × 34 × 3
      ↓
Dilation
      ↓
BGR to RGB Conversion
      ↓
Normalization
      ↓
Flatten to 3468 Features
      ↓
Tuned Random Forest Pipeline
      ↓
A–Z Prediction
      ↓
Confidence Score
