Here's a professional **README.md** based on your paper breakdown that you can use for your GitHub repository.

# Panic Prediction System Using Motion Instability Index (MII)

## Overview

This project presents a lightweight, real-time panic prediction system that forecasts panic events approximately **one second before they occur**. Unlike traditional surveillance systems that only detect panic after it has started, this approach predicts panic by analyzing crowd motion dynamics without using deep learning or GPU acceleration.

---

## Abstract

We developed a panic prediction system that does not rely on machine learning models. By analyzing crowd motion characteristics in real time, the system predicts panic approximately one second before the actual event, enabling faster response and improved public safety.

---

## Problem Statement

Most existing crowd monitoring systems react only after panic has already begun. Threshold-based approaches struggle to distinguish between normal fast movement and genuine panic, while deep learning methods require expensive hardware and large datasets. Our goal is to build a lightweight system capable of predicting panic before it occurs.

---

## System Design

The proposed system extracts three key motion features from each video frame:

* **Speed**
* **Direction Change**
* **Acceleration**

These features are combined into a single metric called the **Motion Instability Index (MII)**.

To improve early detection, each video frame is divided into a **3×3 spatial grid**, allowing the system to identify localized disturbances before they spread across the entire scene.

The system also performs automatic calibration, enabling deployment in different environments without manual parameter tuning.

---

## Implementation

* Language: Python
* Framework: OpenCV
* Hardware Requirement: Standard CPU (No GPU Required)
* Processing Speed: Approximately **33 FPS**
* Platform: Deployable on standard laptops

The lightweight implementation makes the system suitable for real-world surveillance applications.

---

## Results

Experimental evaluation demonstrated that:

* The Motion Instability Index (MII) consistently increased approximately **one second before panic events**.
* High true positive rate with almost zero false negatives.
* Local grid analysis detected panic propagation before the global instability score exceeded the detection threshold.
* Real-time performance was maintained throughout testing.

---

## Key Features

* Real-time panic prediction
* No machine learning or deep learning required
* No GPU dependency
* Lightweight and computationally efficient
* Self-calibrating for different environments
* Localized crowd behavior analysis using a 3×3 spatial grid
* Predicts panic before detection-based systems react

---

## Future Work

Future improvements include:

* Deployment on Raspberry Pi
* Deployment on NVIDIA Jetson Nano
* Integration with CCTV surveillance systems
* SMS and emergency alert notifications
* Multi-camera crowd monitoring

---

## Technologies Used

* Python
* OpenCV
* NumPy
* Optical Flow
* Motion Instability Index (MII)

---

## Repository Structure

```
Dip_Project/
│
├── dataset/
├── models/
├── src/
├── output/
├── results/
├── README.md
└── requirements.txt
```

---

## Conclusion

This project demonstrates that accurate panic prediction does not require computationally expensive deep learning techniques. By combining speed, direction, and acceleration into the Motion Instability Index (MII), the system predicts panic before it occurs while maintaining real-time performance on ordinary hardware. The lightweight design makes it suitable for practical deployment and future edge-device implementations such as Raspberry Pi and Jetson Nano.
