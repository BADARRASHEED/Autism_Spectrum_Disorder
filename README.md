# Autism Prediction Using Machine Learning

## Introduction
This repository contains a **Machine Learning-based Autism Prediction System** that utilizes a **custom-built Random Forest Classifier** to predict whether an individual has **Autism Spectrum Disorder (ASD)** based on behavioral and demographic data. The dataset is sourced from the **REVA University Autism Prediction Challenge** and includes survey responses from over **800 individuals**.

This project aims to **automate the ASD screening process**, reducing the time required for early diagnosis and helping healthcare professionals prioritize cases effectively.

---

## Project Features
✅ **Data Preprocessing**: Handles missing values, categorical encoding, and class imbalance.  
✅ **Exploratory Data Analysis (EDA)**: Includes statistical analysis and visualizations.  
✅ **Custom Machine Learning Model**: Implements a **Random Forest Classifier from scratch**.  
✅ **Model Training & Evaluation**: Achieves an accuracy of **83.75%** with SMOTE oversampling.  
✅ **Saved Model**: The trained classifier is saved for future inference.  

---

## Dataset Overview
The dataset contains **22 features**, including:  
- **Survey-based Autism Quotient (AQ) Scores** (`A1_Score` to `A10_Score`)  
- **Demographic attributes** (`age`, `gender`, `ethnicity`, `country_of_residence`)  
- **Medical history** (`jaundice`, `autism`, `relation`, `used_app_before`)  
- **Target Variable** (`Class/ASD`: `1 = ASD diagnosed`, `0 = Not diagnosed`)  

### Class Distribution Before Balancing
- **ASD Cases (1)**: **230**  
- **Non-ASD Cases (0)**: **570**  
(SMOTE was applied to balance the dataset)  

---

## Technologies & Libraries Used
- **Programming Language**: Python  
- **Libraries Used**:  
  - `numpy`, `pandas` → Data handling  
  - `seaborn`, `matplotlib` → Data visualization  
  - `scikit-learn` → Machine learning utilities  
  - `imblearn` → SMOTE for handling class imbalance  
  - `pickle` → Model and label encoder serialization  

---

## Model Implementation

### 1. Data Preprocessing
- **Missing values handled** in `ethnicity` and `relation` columns.  
- **Label encoding** applied to categorical features.  
- **Outliers detected and replaced** using the **IQR method**.  
- **Class imbalance addressed** using **SMOTE oversampling**.  

### 2. Custom Machine Learning Model
- **Decision Tree Algorithm** implemented from scratch.  
- **Random Forest Classifier** with:  
  - `50` Decision Trees  
  - `Max Depth: 10`  
  - `Bootstrap Sampling`  
  - `Feature Subset Ratio: 60%`  

### 3. Model Training & Evaluation
- **Train-Test Split**: **80% Training, 20% Testing**  
- **Performance Metrics**:  
  - **Accuracy**: **83.75%**  
  - **Precision (ASD=1)**: **61%**  
  - **Recall (ASD=1)**: **75%**  
  - **F1-score (ASD=1)**: **67%**  

### 4. Model Saving
- The trained **Random Forest model** is saved as `custom_rf_model.pkl`.  
- Label encoders for categorical variables are saved in `encoders.pkl`.  

---

## How to Use This Project

### 1. Clone the Repository
```bash
git clone https://github.com/BADARRASHEED/Autism_Spectrum_Disorder.git
cd Autism_Spectrum_Disorder
