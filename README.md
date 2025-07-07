# Lung Cancer Prediction

This project is focused on predicting lung cancer survival status using a dataset from the Idealize 2025 Datathon competition.

## Project Structure

- `metamorphs (1).ipynb`: Main Jupyter notebook containing all data loading, preprocessing, feature engineering, and modeling code.
- `README.md`: Project overview and instructions.

## Workflow Overview

### 1. Data Loading

The notebook loads the training data from `/kaggle/input/idealize-2025-datathon-competition/train.csv` and the test data from `/kaggle/input/idealize-2025-datathon-competition/test.csv`.

### 2. Data Cleaning & Preprocessing

- Drops unnecessary columns: `first_name`, `last_name`, `record_id`.
- Fills missing values in `cigarettes_per_day` for non-smokers.
- Encodes binary columns (`family_cancer_history`, `has_other_cancer`, `asthma_diagnosis`, `liver_condition`, `blood_pressure_status`, `sex`) as 0/1.
- Standardizes and one-hot encodes categorical columns (`smoking_status`, `treatment_type`).
- Drops `residence_state` after encoding.
- Converts date columns to datetime and creates new features: `treatment_duration` and `diagnosis_to_treatment_delay`.

### 3. Feature Engineering

- Custom transformers (`ProcessSmoking`, `ProcessCols`, `EncodeCatCols`, `FormatDates`) are defined for use in a scikit-learn pipeline.
- The pipeline automates all preprocessing steps for both training and test data.

### 4. Modeling

- The notebook includes commented-out code for training and evaluating several models:
  - Logistic Regression
  - Random Forest
  - K-Nearest Neighbors
  - Neural Network (TensorFlow/Keras)
- Model evaluation is performed using accuracy score.

### 5. Visualization

- (Optional) Code for plotting training and validation accuracy curves using matplotlib is included but commented out.

## How to Run

1. Open `metamorphs (1).ipynb` in Jupyter or VS Code.
2. Run each cell sequentially to preprocess the data and train models.
3. Modify or uncomment model training cells as needed for experimentation.

## Requirements

- Python 3.11+
- pandas, numpy, scikit-learn, matplotlib, tensorflow (for neural network)

## Notes

- The notebook is designed for use in a Kaggle environment, with data files loaded from `/kaggle/input/`.
- All preprocessing steps are encapsulated in reusable classes for cleaner code and easier experimentation.

---

For more details, see the code and comments in [metamorphs (1).ipynb](metamorphs%20(1).ipynb).