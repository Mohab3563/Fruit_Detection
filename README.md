#  Fruit Detection and Classification Using Deep Learning

A comprehensive computer vision system for detecting and classifying fruits in static images. This project leverages classical image processing techniques and deep learning models to identify multiple fruit objects, draw bounding boxes, and classify them using a custom-trained CNN. A graphical user interface (GUI) is included for ease of use.

---

## 📌 Overview

This project aims to build an end-to-end pipeline for automated fruit recognition using image processing and convolutional neural networks. The system supports the following features:

- Image preprocessing and enhancement
- Fruit object segmentation and contour extraction
- Deep feature extraction using MobileNetV2
- Classification using a custom CNN
- Real-time image-based detection via a Tkinter GUI

---

## 📂 Dataset

- **Name:** Custom Fruit Dataset  
- **Source:** [Kaggle - Fruit Images Dataset](https://www.kaggle.com/datasets/shreyapmaher/fruits-dataset-images)  
- **Classes:** 9 fruit categories (e.g., Apple, Banana, Orange, etc.)  
- **Augmentation:** Manual augmentation to enhance class balance and robustness  
- **Format:** Organized into training and test sets by class labels

---

## 🧪 Methodology

### 🔧 Preprocessing & Enhancement
- Resize to 224×224 pixels
- HLS contrast enhancement
- Gaussian blurring & sharpening
- Grayscale conversion
- Otsu’s thresholding
- Morphological operations (opening & closing)

### 🔍 Segmentation
- Watershed algorithm to separate touching fruit objects
- Contour detection to extract object boundaries and ROIs

### 📐 Feature Extraction
- MobileNetV2 (pretrained on ImageNet) used as a feature extractor (excluding top layers)
- Features extracted from segmented ROI crops

### 🧠 Classification
- A custom CNN was trained using extracted features
- Output labels include the fruit class name for each detected object

### 🧾 Evaluation Metrics
- Accuracy: >95% on test data
- Precision, Recall, F1-Score
- Confusion Matrix and classification report

---

## 💻 Graphical User Interface (GUI)

The system includes an intuitive GUI built with **Tkinter** that allows users to:
- Upload an image
- Perform fruit detection with one click
- Visualize bounding boxes and predicted class labels directly on the image

---

## 🛠 Installation

### 🔗 Prerequisites

Ensure Python 3.x is installed. Then install the required packages:

```bash
pip install -r requirements.txt
