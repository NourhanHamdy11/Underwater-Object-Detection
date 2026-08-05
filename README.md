# 🌊 Underwater Object Detection using YOLOv8 & Faster R-CNN

# Table of Contents

- Overview
- Project Objectives
- Related Work
- Dataset
- Dataset Statistics
- Data Preprocessing
- Model Architectures
- Training Pipeline
- Evaluation Metrics
- Experimental Results
- Repository Structure
- Technologies Used
- Installation
- Usage
- Future Improvements
- Team Members
- References

---

# Overview

This project presents a deep learning solution for underwater object detection and localization.

The main objective is to compare multiple convolutional neural network architectures for detecting marine objects in underwater environments.

Two state-of-the-art object detection models were implemented and evaluated:

- Faster R-CNN with ResNet-50
- YOLOv8

The project also investigates different preprocessing techniques, data augmentation methods, and image color spaces to improve detection performance.

---

# Project Objectives

- Detect underwater objects accurately.
- Localize objects using bounding boxes.
- Compare Faster R-CNN and YOLOv8.
- Improve model performance using image preprocessing.
- Evaluate model performance using precision and recall.

---

# Related Work

A literature search revealed very limited research using the same dataset.

Existing resources included:

- One Roboflow notebook using YOLOv8.
- No significant Kaggle notebooks using the same dataset.

Therefore, this project contributes additional experimental comparisons and performance improvements.

---

# Dataset

The project uses an underwater object detection dataset containing annotated images with bounding boxes.

## Dataset Information

| Property | Value |
|----------|-------|
| Images | 798 |
| Classes | 7 |
| Annotation | Bounding Boxes |
| Annotation Tool | Roboflow |

---

# Classes

- Fish
- Crab
- Human
- Trash
- Jellyfish
- Coral Reef
- Fish Group

---

# Dataset Split

| Dataset | Percentage |
|----------|-----------|
| Training | 70% |
| Validation | 10% |
| Testing | 20% |

---

# Training Set Distribution

| Class | Images |
|--------|--------|
| Fish | 234 |
| Human | 112 |
| Fish Group |108|
| Trash |87|
| Crab |83|
| Coral Reef |83|
| Jellyfish |72|

### Dataset Challenges

- Small dataset size
- Imbalanced classes
- Limited samples for some categories

To overcome these limitations, extensive data augmentation was performed.

Training images increased from:

**559 ➜ 3354 Images**

---

# Data Preprocessing

## Data Augmentation

The following augmentation techniques were applied:

- Horizontal Flip
- Rotation (90°)
- Rotation (180°)
- Rotation (270°)

Bounding boxes were transformed together with every augmented image.

---

## YOLO Annotation Conversion

Bounding boxes were converted into YOLO format:

- Center X
- Center Y
- Width
- Height

---

## Color Space Optimization

Instead of training directly on RGB images, images were converted into the HLS color space.

Multiple experiments showed that HLS images produced better detection performance.

---

# Model Architectures

## Faster R-CNN

Backbone:

- ResNet-50

Why ResNet?

Residual learning helps overcome the vanishing gradient problem while enabling deeper neural networks with better feature extraction.

Advantages

- Accurate localization
- High detection accuracy
- Strong feature representation

---

## YOLOv8

YOLOv8 is one of the latest versions of the YOLO family.

Advantages

- Real-time object detection
- Fast inference
- Lightweight architecture
- High precision

---

## Additional Experiment

A VGG16 classifier with a custom classification head was also tested.

However, its performance was considerably lower than both YOLOv8 and Faster R-CNN.

---

# Training Pipeline

Dataset

↓

Data Augmentation

↓

Color Space Conversion (RGB → HLS)

↓

Bounding Box Processing

↓

Model Training

↓

Validation

↓

Testing

↓

Performance Evaluation

---

# Evaluation Metrics

Performance was evaluated using:

- Training Accuracy
- Validation Accuracy
- Precision
- Recall

---

# Experimental Results

## Faster R-CNN + ResNet-50

| Metric | Score |
|---------|------|
| Precision | **85%** |
| Recall | **84%** |

---

## YOLOv8

YOLOv8 achieved higher precision than the available benchmark using the same dataset.

---

# Performance Comparison

| Model | Precision | Recall |
|--------|-----------|--------|
| Faster R-CNN | **85%** | **84%** |
| Online Benchmark |79.7%|63%|

---

# Visual Results

The project includes:

- Training Accuracy Curve
- Validation Accuracy Curve
- Confusion Matrix
- Precision & Recall Graphs

*(Insert figures here if available.)*

---

# Repository Structure

```
Underwater-Object-Detection/
│
├── Dataset/
├── Models/
├── Training/
├── Evaluation/
├── Results/
├── Figures/
├── README.md
└── requirements.txt
```

---

# Technologies Used

- Python
- TensorFlow
- PyTorch
- Keras
- OpenCV
- NumPy
- Matplotlib
- Roboflow

---

# Installation

```bash
git clone https://github.com/yourusername/underwater-object-detection.git

cd underwater-object-detection

pip install -r requirements.txt
```

---

# Usage

Run the training pipeline:

```bash
python train.py
```

Run evaluation:

```bash
python evaluate.py
```

---

# Future Improvements

- Increase dataset size.
- Improve class balancing.
- Train for more epochs.
- Hyperparameter optimization.
- Test newer YOLO architectures.
- Deploy as a real-time underwater monitoring application.



---

# References

- Roboflow Underwater Dataset
- Kaggle Underwater Dataset
- Keras Applications Documentation

---

⭐ If you find this project useful, consider giving it a star.
