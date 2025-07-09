# patient_readmission_project
Patient Readmission Risk Prediction

📊 Project Overview

This project analyzes patient demographic information, diagnoses, procedures, and hospital visit details to predict the likelihood of patient readmission within 30 days. The solution helps hospitals proactively identify at-risk patients and improve care coordination through data-driven insights.

📂 Data Source

The dataset comes from the Health Facts database (Cerner Corporation) and contains 10 years of clinical care data from 130 US hospitals. 
Key features include:
Demographic information
Diagnosis codes (ICD-9)
Medication details
Hospital utilization metrics
Laboratory results

Link:https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008

⚙️ Installation

To run this project:

# Clone repository
git clone https://github.com/Yugalchaudhary01/patient_readmission_project.git

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate    # Windows

# Install dependencies
pip install -r requirements.txt

🧠 Methodology

Data Preprocessing

Missing Values: Removed columns with >40% missing data
Invalid Records: Filtered out deceased patients and unknown genders
Feature Engineering:
Created primary diagnosis categories from ICD-9 codes
Added medication change flag
Categorized hospital stay durations
Target Variable: Binary readmission flag (<30 days)

Model Development
Model	Description	Key Parameters
Logistic Regression	Baseline model	Class weighting for imbalance
Random Forest	Advanced ensemble	150 trees, balanced classes

Evaluation Metrics
Accuracy, Precision, Recall, F1-Score

ROC-AUC and Confusion Matrix

Classification Reports


📊 Results
Model Performance Comparison

Model	                Accuracy	Precision	Recall	F1-Score	ROC-AUC
Logistic Regression	    0.632	    0.314	    0.593	0.412	    0.647
Random Forest	        0.681	    0.378	    0.642	0.479	    0.721

Key Findings
Top Predictive Features:

Number of inpatient visits
Number of medications
Primary diagnosis (Circulatory issues)
Time in hospital
Number of lab procedures

High-Risk Patient Profile:

Previous inpatient admissions
Taking >20 medications
Circulatory system diagnosis
Long hospital stays (8+ days)



📚 References
Strack et al. (2014). "Diabetes 130-US hospitals dataset"

Centers for Medicare & Medicaid Services. (2023). "Hospital Readmissions Reduction Program"

American Diabetes Association. (2022). "Standards of Medical Care in Diabetes"

