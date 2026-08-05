# 🌊 Underwater Object Detection using YOLOv8 & Faster R-CNN

## 📖 Overview

This project focuses on detecting and localizing underwater objects using state-of-the-art deep learning models.

The project compares two powerful object detection approaches:

- YOLOv8
- Faster R-CNN with ResNet-50 backbone

The models were trained and evaluated on a custom underwater dataset containing multiple marine object classes.

---

## 🎯 Project Objectives

- Detect underwater objects accurately.
- Compare the performance of modern object detection architectures.
- Improve detection accuracy using data augmentation and image preprocessing.
- Evaluate different CNN-based approaches.

---

## 🗂 Dataset

Dataset Characteristics:

- 798 labeled underwater images
- 7 object classes
- Bounding box annotations
- Roboflow annotation format

### Classes

- Fish
- Fish Group
- Crab
- Coral Reef
- Jellyfish
- Human
- Trash

Dataset Split

| Set | Percentage |
|------|------------|
| Training | 70% |
| Validation | 10% |
| Testing | 20% |

---

## 🔧 Data Preprocessing

Several preprocessing techniques were applied to improve model performance.

### Data Augmentation

- Horizontal Flip
- Random Rotation (90°, 180°, 270°)

Bounding boxes were transformed together with each image.

### Image Processing

- RGB → HLS color conversion
- YOLO bounding box conversion
- Dataset balancing through augmentation

Training images increased from:

**559 → 3,354 images**

---

## 🤖 Models

### 1. Faster R-CNN

Backbone:

- ResNet-50

Advantages:

- High localization accuracy
- Strong feature extraction
- Suitable for complex underwater scenes

---

### 2. YOLOv8

Features:

- Real-time object detection
- Lightweight architecture
- High inference speed
- Multi-class detection

---

### Additional Experiment

A VGG16-based CNN classifier was tested.

However, its performance was significantly lower than both Faster R-CNN and YOLOv8.

---

## 📊 Evaluation Metrics

The following metrics were used:

- Precision
- Recall
- Training Accuracy
- Validation Accuracy

---

## 📈 Results

### Faster R-CNN (ResNet-50)

- Precision: **85%**
- Recall: **84%**

### YOLOv8

Achieved higher precision than the available benchmark on the same dataset.

---

## 🚀 Technologies Used

- Python
- TensorFlow
- Keras
- PyTorch
- OpenCV
- Roboflow
- NumPy
- Matplotlib

---

## 📚 References

- Roboflow Underwater Dataset
- Kaggle Underwater Dataset
- Keras Applications Documentation

---


## 📌 Future Improvements

- Increase dataset size.
- Improve class balancing.
- Train for more epochs.
- Experiment with newer YOLO versions.
- Apply advanced augmentation techniques.
- Deploy the model as a real-time application.

---

## ⭐ Project Highlights

✔ Underwater Object Detection

✔ YOLOv8 Implementation

✔ Faster R-CNN with ResNet-50

✔ Data Augmentation

✔ Image Preprocessing

✔ Performance Evaluation

✔ Deep Learning
