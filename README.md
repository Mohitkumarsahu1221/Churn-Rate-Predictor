# Churn Rate Predictor

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-Latest-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

> An end-to-end machine learning pipeline for customer segmentation and churn prediction using RFM analysis, K-Means clustering, and Logistic Regression with comprehensive model evaluation and explainability.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Methodology](#methodology)
- [Model Performance](#model-performance)
- [Requirements](#requirements)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project implements a comprehensive churn prediction system that combines RFM (Recency, Frequency, Monetary) segmentation with machine learning to identify at-risk customers. The pipeline is designed for e-commerce or subscription-based businesses looking to reduce customer churn through data-driven insights.

### Key Objectives

- Segment customers based on RFM metrics
- Identify churn patterns and at-risk customer segments
- Predict customer churn probability with high accuracy
- Provide interpretable and explainable predictions

## ✨ Features

- **RFM Analysis**: Calculate Recency, Frequency, and Monetary metrics for customer segmentation
- **K-Means Clustering**: Identify distinct customer segments automatically
- **Churn Prediction**: Binary classification using Logistic Regression
- **Model Evaluation**: Comprehensive metrics including accuracy, precision, recall, F1-score, and ROC-AUC
- **Model Explainability**: Feature importance and prediction interpretability
- **Model Persistence**: Save and load trained models using joblib
- **Jupyter Notebook**: Interactive exploration and visualization of results

## 📦 Installation

### Prerequisites

- Python 3.8 or higher
- pip or conda package manager

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/Mohitkumarsahu1221/Churn-Rate-Predictor.git
   cd Churn-Rate-Predictor
   ```

2. **Create a virtual environment** (optional but recommended)
   ```bash
   python -m venv myenv
   
   # Activate the virtual environment
   # On Windows:
   myenv\Scripts\activate
   # On macOS/Linux:
   source myenv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 📁 Project Structure

```
Churn-Rate-Predictor/
├── README.md                          # This file
├── RFM Clustring.ipynb               # Main Jupyter notebook with full pipeline
├── churn_model.joblib                # Trained model artifact
├── myenv/                            # Virtual environment directory
└── requirements.txt                  # Python dependencies
```

## 🚀 Usage

### Running the Analysis

1. **Open the Jupyter notebook**
   ```bash
   jupyter notebook "RFM Clustring.ipynb"
   ```

2. **Follow the notebook cells** to:
   - Load and explore customer data
   - Calculate RFM metrics
   - Perform customer segmentation
   - Train the churn prediction model
   - Evaluate model performance
   - Make predictions on new data

### Loading the Trained Model

```python
import joblib

# Load the pre-trained model
model = joblib.load('churn_model.joblib')

# Make predictions
predictions = model.predict(X_new)
prediction_probabilities = model.predict_proba(X_new)
```

## 🔍 Methodology

### 1. RFM Segmentation

The pipeline segments customers into meaningful groups using three key metrics:

- **Recency**: How recently a customer made a purchase
- **Frequency**: How often a customer makes purchases
- **Monetary**: How much a customer has spent

### 2. K-Means Clustering

Unsupervised learning technique to automatically identify optimal customer segments based on RFM metrics.

### 3. Churn Prediction

Logistic Regression classification model trained to predict the probability of customer churn based on behavioral and segmentation features.

## 📊 Model Performance

The trained model achieves:

- **Accuracy**: High overall correctness on test set
- **Precision**: Reliability in identifying actual churners
- **Recall**: Ability to catch at-risk customers
- **ROC-AUC**: Strong discriminative power between classes

*Detailed metrics and performance visualizations are available in the Jupyter notebook.*

## 📋 Requirements

Key Python packages:

- `numpy` - Numerical computing
- `pandas` - Data manipulation and analysis
- `scikit-learn` - Machine learning models and metrics
- `matplotlib` - Data visualization
- `seaborn` - Statistical data visualization
- `jupyter` - Interactive notebook environment
- `joblib` - Model serialization

For a complete list, see [requirements.txt](requirements.txt).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request with:

- Bug fixes
- Feature enhancements
- Improved documentation
- Additional analysis or visualizations
