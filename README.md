# Kannada MNIST Classification using PCA and KNN

## Project Overview

This project implements handwritten Kannada digit classification using **Principal Component Analysis (PCA)** for dimensionality reduction and **K-Nearest Neighbors (KNN)** for classification.

The complete workflow is documented in the Jupyter Notebook [`intern.ipynb`](intern.ipynb), including dataset loading, preprocessing, PCA, KNN prediction, evaluation, and class-wise accuracy visualization.

## Dataset

The notebook works with the Kannada-MNIST handwritten digit dataset.

- Training samples: **60,000**
- Test samples: **10,000**
- Image size: **28 × 28 pixels**
- Classes: **10 Kannada digit classes (0–9)**
- Training data contains **784 pixel features** after flattening
- No missing values were found in the dataset

## Methodology

### 1. Data Preprocessing

- Pixel values are converted from integer format to `float32`.
- Pixel values are normalized from **0–255 to 0–1**.
- Each 28 × 28 image is flattened into **784 features**.

### 2. Principal Component Analysis (PCA)

PCA is applied to reduce the dimensionality while retaining 95% of the variance.

- Original features: **784**
- Reduced features: **237**
- Explained variance retained: **95.02%**

### 3. KNN Classification

A K-Nearest Neighbors classifier is trained using the PCA-transformed data.

- Algorithm: **K-Nearest Neighbors (KNN)**
- Number of neighbors (`k`): **3**
- Prediction is performed on the PCA-transformed test data.

## Results

The model achieved:

**KNN Accuracy: 92.55%**

The notebook also includes a classification report with precision, recall, F1-score, and support for each digit class, along with a class-wise accuracy graph.

### Classification Report Summary

| Metric | Score |
|---|---:|
| Accuracy | **92.55%** |
| Macro Precision | **93%** |
| Macro Recall | **93%** |
| Macro F1-score | **93%** |

## Technologies Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- PCA
- K-Nearest Neighbors (KNN)

## Project Workflow

```text
Kannada MNIST Dataset
        ↓
Data Loading
        ↓
Normalization
        ↓
Flatten 28×28 Images → 784 Features
        ↓
PCA (95% Variance)
        ↓
784 Features → 237 Features
        ↓
KNN (k = 3)
        ↓
Prediction
        ↓
Accuracy & Classification Report
        ↓
Class-wise Accuracy Visualization
```

## Notebook

Open the complete implementation here:

[**intern.ipynb**](intern.ipynb)

## Result

The combination of **PCA for dimensionality reduction** and **KNN for classification** achieved an accuracy of **92.55%** on the Kannada-MNIST test set.
