# patient_readmission_project
Patient Readmission Risk Prediction

📊 Project Overview

This project will include the analysis of the demographics, diagnosis, procedures, and details of the visits made to the hospital to predict the risk of the patient being readmitted to the hospital in 30 days. The solution assists hospitals in the active identification of at-risk patients and data-driven care coordination.

📂 Data Source

Data are obtained on the Health Facts database (Cerner Corporation) that comprises 10-year data on clinical care through 130 US hospitals. 
Important characteristics are:
Demographic information
Diagnosis codes (ICD-9)
Medication Metrics
Hospital utilization 
Laboratory results

Link:https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008

⚙️ Installation

To run this project:

# Clone repository
git clone https://github.com/Yugalchaudhary01/patient_readmission_project.git

# Design virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate    # Windows

# Install dependencies
pip install -r requirements.txt

🧠 Methodology

Data Preprocessing

Missing Values: Dropped columns that had more than 40 percent of missing data 
Invalid Records: Filtered out deaths and unknown gender 
Incomplete Data: Created medication change flag created categories of the primary diagnosis based on the ICD-9 codes Categorized length of hospital stay 
Dropped data that remained null Coded readmission outcome as a binary feature with over 30 days as 0 (no readmission) and anything less than 30 days as 1 (readmission)

Model Development
 Model Description Key Parameters Logistic regression 
 Base Generator model Class weighting imbalance Random forest Enhanced ensemble 150 trees balanced classes

Evaluation metrics are Accuracy, Precision, recall, F1-Score

ROC-AUC and Confusion Matrix

Classification Reports


📊 Results
Model Performance Comparison

Model	                Accuracy	Precision	Recall	F1-Score	ROC-AUC
Logistic Regression	    0.632	    0.314	    0.593	0.412	    0.647
Random Forest	        0.681	    0.378	    0.642	0.479	    0.721

Key Findings
Top Predictive Features:

Length of inpatient stays 
Number of medication 
Number of primary diagnosis (Circulatory problems) Length of stay in hospital 
Number of lab test that a patient undergoes

Patient at risk Profile:

Past inpatient visit Receiving more than 20 medications Cardiovascular disease diagnosis Lengthy stays in hospital (more than 8 days)

📚 References
Strack et al. (2014). "Diabetes 130-US hospitals dataset"

Centers for Medicare & Medicaid Services. (2023). "Hospital Readmissions Reduction Program"

American Diabetes Association. (2022). "Standards of Medical Care in Diabetes"

