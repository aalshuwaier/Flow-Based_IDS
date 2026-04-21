**Flow-Based Intrusion Detection System (IDS) - NSL-KDD**

*ECE 57000 Course Project - Track 2: Product Prototype*

## Project Overview

This project implements a flow-based Intrusion Detection System (IDS) that classifies network traffic into five categories:

- **Normal**: benign traffic
- **DoS**: Denial of Service attacks
- **Probe**: surveillance/probing attacks
- **R2L**: Remote-to-Local attacks
- **U2R**: User-to-Root attacks

The target user is a network security analyst who needs an automated first-passfilter to classify incoming network flows.

## Dataset

- **NSL-KDD** (publicly available from the University of New Brunswick)
- The dataset is automatically downloaded from GitHub in the notebook (Section 2).
  No manual download is required.
- Training set: 125,973 samples 
- Test set: 22,544 samples

## Code Structure

The project is implemented as a single Jupyter notebook (`ECE57000_project.ipynb`).

| Section | Description |
|---------|-------------|
| 1 | Install & Import |
| 2 | Load NSL-KDD Dataset |
| 3 | Preprocessing |
| 4 | Random Forest Baseline |
| 5 | Confusion Matrix & Feature Importance Visualization |
| 6 | Binary Classification (Normal vs Attack) |
| 7 | XGBoost with Class Weights |
| 8 | Random Forest with class_weight='balanced' |
| 9 | MLP (Neural Network) |
| 10 | CP2 Comparison Table & Visualization |
| 11 | MLP with Class Balancing |
| 12 | SMOTE (Synthetic Minority Oversampling) |
| 13 | Feature Selection using XGBoost Importance | 
| 14 | Final Comparison (All Models) | 
| 15 | XGBoost+SMOTE Model Confusion Matrix |
| 16 | Prototype - IDS Prediction Interface |

## Dependencies

```
python >= 3.8
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
imbalanced-learn
```

Install with:
```
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn
```

## How to Run

1. Open `ECE57000_project.ipynb` in Google Colab (recommended) or Jupyter Notebook.
2. Run all cells sequentially from Section 1 through Section 18.
   - The dataset is automatically downloaded in Section 2 (no manual download needed).
   - All dependencies are available by default in Google Colab; if running locally, install them with the command above.
3. Results (tables and figures) are generated inline.
4. The prototype interface is demonstrated at the end of Section 16.

## Acknowledgement

- **Written by me:** All code in the notebook, including data loading, preprocessing, model training (RF, XGBoost, MLP), evaluation, class imbalance handling (sample weights, oversampling, SMOTE), feature selection, and the prototype.

- **Adapted from:** scikit-learn and XGBoost documentation examples for model training API patterns and evaluation metric usage.

- **Copied from:** None. No code was directly copied from external repositories.

- **LLM assistance:** LLM was used as a coding assistant throughout the entire project for code debugging, experimental design, generating code to visualize results, and report drafting.
