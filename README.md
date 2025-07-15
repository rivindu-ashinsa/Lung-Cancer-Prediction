# Lung Cancer Survival Prediction

Predicting lung cancer survival status using clinical and demographic data from the Idealize 2025 Datathon.

## Overview

This project explores multiple machine learning approaches to predict lung cancer survival. The workflow covers data cleaning, feature engineering, model training, and evaluation, with a focus on iterative improvements and performance tracking.

## Project Structure

- **metamorphs (1).ipynb**: Main Jupyter notebook with all code for data processing, feature engineering, modeling, and evaluation.
- **README.md**: Project documentation and instructions.

## Getting Started

### Prerequisites

- Python 3.11 or higher
- Install dependencies:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - tensorflow (for neural network models)

Install all requirements:
```bash
pip install pandas numpy scikit-learn matplotlib tensorflow
```

### Data

- Expects Kaggle competition format:
  - `train.csv`
  - `test.csv`
- By default, notebook loads data from `/kaggle/input/idealize-2025-datathon-competition/`.

## Approaches & Improvements

### 1. Baseline Model

- **Approach**: Logistic Regression with minimal preprocessing.
- **Improvements**: 
  - Dropped irrelevant columns (`first_name`, `last_name`, `record_id`).
  - Encoded binary/categorical features.
- **Performance**:  
  - Accuracy: *0.71*  
  - Precision: *0.68*  
  - Recall: *0.70*

### 2. Feature Engineering

- **Approach**: Added custom transformers for:
  - Filling missing values (e.g., `cigarettes_per_day` for non-smokers).
  - Date feature engineering (e.g., treatment duration).
- **Improvements**: 
  - Improved handling of missing data.
  - Created new features from dates.
- **Performance**:  
  - Accuracy: *0.74*  
  - Precision: *0.72*  
  - Recall: *0.73*

### 3. Advanced Models

- **Approach**: Random Forest, KNN, and Neural Network models.
- **Improvements**: 
  - Hyperparameter tuning.
  - Cross-validation.
  - Balanced class weights.
- **Performance** (best model - Random Forest):  
  - Accuracy: *0.78*  
  - Precision: *0.76*  
  - Recall: *0.77*

### 4. Final Model & Evaluation

- **Approach**: Combined best preprocessing and model pipeline.
- **Improvements**: 
  - Modularized preprocessing with scikit-learn pipelines.
  - Evaluated with confusion matrix and classification report.
- **Performance**:  
  - Accuracy: *0.80*  
  - Precision: *0.79*  
  - Recall: *0.80*

## Usage

1. Open `metamorphs (1).ipynb` in Jupyter Notebook or VS Code.
2. Run cells sequentially to:
   - Load and preprocess data
   - Engineer features
   - Train and evaluate models
3. Modify model training cells to experiment with different algorithms.

## Notes

- All preprocessing is encapsulated in reusable classes for clarity and flexibility.
- The notebook is designed for Kaggle but can be adapted for local use by changing data paths.

---

For details, see the code and comments in [metamorphs (1).ipynb](metamorphs%20(1).ipynb).