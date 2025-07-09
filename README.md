# Lung Cancer Survival Prediction

Predicting lung cancer survival status using clinical and demographic data from the Idealize 2025 Datathon.

## Overview

This repository contains code and resources for building machine learning models to predict lung cancer survival. The workflow includes data cleaning, feature engineering, model training, and evaluation, all implemented in a modular and reproducible manner.

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

You can install all requirements with:
```bash
pip install pandas numpy scikit-learn matplotlib tensorflow
```

### Data

- The project expects data in the Kaggle competition format:
  - `train.csv`
  - `test.csv`
- By default, the notebook loads data from `/kaggle/input/idealize-2025-datathon-competition/`.

### Running the Project

1. Open `metamorphs (1).ipynb` in Jupyter Notebook or VS Code.
2. Run cells sequentially to:
   - Load and preprocess data
   - Engineer features
   - Train and evaluate models
3. Uncomment or modify model training cells to experiment with different algorithms.

## Workflow Summary

1. **Data Loading**: Import training and test datasets.
2. **Preprocessing**:
   - Drop irrelevant columns (`first_name`, `last_name`, `record_id`)
   - Handle missing values (e.g., fill `cigarettes_per_day` for non-smokers)
   - Encode binary and categorical features
   - Convert and engineer date features (e.g., treatment duration)
3. **Feature Engineering**: Use custom scikit-learn transformers for streamlined preprocessing.
4. **Modeling**: Train and evaluate models such as Logistic Regression, Random Forest, KNN, and Neural Networks.
5. **Visualization**: (Optional) Plot training/validation metrics.

## Notes

- All preprocessing is encapsulated in reusable classes for clarity and flexibility.
- The notebook is designed for Kaggle but can be adapted for local use by changing data paths.

---

For details, see the code and comments in [metamorphs (1).ipynb](metamorphs%20(1).ipynb).