# Alzheimer's MRI CNN Classification

## Overview

This project focuses on classifying different stages of Alzheimer’s disease using brain MRI images and deep learning techniques. The goal is to build and evaluate Convolutional Neural Network (CNN) models that can accurately distinguish between multiple stages of cognitive decline.

The project includes multiple CNN-based approaches, data preprocessing techniques, data augmentation, and transfer learning using a pre-trained model.

---

## Problem Statement

Alzheimer’s disease is a progressive neurological disorder that affects memory and cognitive function. Early and accurate detection is critical for treatment and management.

This project aims to classify MRI brain scans into five categories:
- Alzheimer’s Disease (AD)
- Cognitively Normal (CN)
- Early Mild Cognitive Impairment (EMCI)
- Late Mild Cognitive Impairment (LMCI)
- Mild Cognitive Impairment (MCI)

---

## Dataset

The dataset used in this project consists of brain MRI images for Alzheimer’s disease classification. The dataset was provided for academic use and is derived from publicly available neuroimaging sources such as the Alzheimer’s Disease Neuroimaging Initiative (ADNI).

The images are organized into five classes representing different stages of cognitive decline:

- Alzheimer’s Disease (AD)
- Cognitively Normal (CN)
- Early Mild Cognitive Impairment (EMCI)
- Late Mild Cognitive Impairment (LMCI)
- Mild Cognitive Impairment (MCI)

Each class contains MRI scans that were preprocessed and converted into JPEG image format for use in deep learning models.

---

## Dataset Structure
├── Final AD JPEG/
├── Final CN JPEG/
├── Final EMCI JPEG/
├── Final LMCI JPEG/
├── Final MCI JPEG/


---

## Data Preparation

- Dataset loaded from Google Drive using Google Colab
- Images resized to 224x224 pixels
- Pixel values normalized (rescaled by 1/255)
- Dataset split into training, validation, and test sets
- Data augmentation techniques applied:
  - Rotation
  - Width and height shifts
  - Zoom
  - Horizontal flipping

---

## Models Implemented

### 1. Baseline CNN
- Convolutional layers with ReLU activation
- Batch normalization
- Max pooling layers
- Fully connected layers with dropout
- Softmax output layer

---

### 2. CNN with Normalization
- Applied feature normalization to improve model stability
- Same architecture as baseline with improved preprocessing

---

### 3. CNN with Data Augmentation
- Trained using augmented data to improve generalization
- Reduced overfitting compared to baseline model

---

### 4. Transfer Learning (MobileNetV2)
- Pre-trained MobileNetV2 used as feature extractor
- Base model frozen
- Added custom classification layers
- Improved feature extraction from MRI images

---

## Overfitting Mitigation Techniques

- Dropout layers
- Data augmentation
- Early stopping
- Batch normalization

---

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## Results

| Model                     | Accuracy |
|--------------------------|--------|
| Baseline CNN             | ~44%   |
| CNN + Augmentation       | ~45%   |
| Transfer Learning Model  | ~45%   |

### Observations
- Models showed limited performance due to dataset complexity
- Some classes were harder to distinguish, leading to imbalance in predictions
- Transfer learning slightly improved performance

---

## Tools & Technologies

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

