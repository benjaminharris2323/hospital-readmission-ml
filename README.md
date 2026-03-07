# Predicting 30-Day Hospital Readmissions Using Interpretable Machine Learning

This project develops an interpretable machine learning model to predict 30-day hospital readmissions using structured electronic health record (EHR) data.

## Dataset

UCI Machine Learning Repository  
Diabetes 130-US hospitals dataset (1999-2008)

Dataset source: https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008

## Goal

Identify patients at elevated risk of readmission using interpretable features derived from clinical utilization patterns.

## Models Evaluated

- Logistic Regression (baseline + tuned)
- Random Forest
- Histogram Gradient Boosting

## Final Model

Tuned Logistic Regression with class weighting and threshold optimization.

Performance:

- ROC-AUC ≈ 0.65
- Recall ≈ 0.53
- Precision ≈ 0.17

## Key Findings

Readmission risk is primarily driven by utilization intensity and clinical complexity:

- Prior inpatient visits
- Emergency visits
- Number of procedures
- Medication burden

Tree-based models produced only marginal improvements in ROC-AUC while reducing interpretability.

## Calibration

Model calibration was evaluated using reliability curves and Brier scores.

Lower thresholds substantially increased recall for screening scenarios.

## Repository Structure

hospital-readmission-ml
│
├── A1C_clinical_significance_and_severity_proxy.pdf
├── readmission_model.ipynb
├── refined_documentation.pdf
├── final_readmission_model.joblib
├── requirements.txt



## Running the Project

Install dependencies:

pip install -r requirements.txt

Run the notebook:

jupyter notebook readmission_model.ipynb


## Author

Ben Harris  
MS Business Analytics – University of Cincinnati  
Data Science | Machine Learning | Healthcare Analytics


