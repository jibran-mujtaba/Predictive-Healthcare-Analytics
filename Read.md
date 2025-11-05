Diabetes 130-US Hospitals Readmission Analysis

This repository contains an analysis of the Diabetes 130-US hospitals readmission dataset from the UCI Machine Learning Repository
. The dataset includes 10 years (1999–2008) of clinical care at 130 US hospitals and integrated delivery networks, representing over 100,000 diabetic patient hospital encounters.

📂 Repository Structure
├── diabetic_data.csv   # Dataset (UCI Diabetes Readmission Dataset)
├── Main.ipynb          # Jupyter Notebook with analysis and modeling
└── README.md           # Project documentation

📊 Dataset Overview

Rows: 101,766 patient encounters

Columns: 50 features including demographics, diagnoses, lab results, and medications

Target: Patient readmission status

0: Not readmitted

1: Readmitted within 30 days

Class Distribution (Imbalanced)

Not Readmitted: ~89%

Readmitted (within 30 days): ~11%
⚠️ The dataset is highly imbalanced, which impacts predictive modeling.

Key Features

Patient demographics (race, gender, age)

Admission type, discharge disposition, admission source

Diagnoses (ICD-9 codes)

Number of procedures, medications, and lab results

Readmission outcome

🎯 Project Goals

Data Cleaning & Preprocessing

Handle missing values and categorical features

Encode categorical variables

Normalize/scale numerical features

Exploratory Data Analysis (EDA)

Distribution of demographics & hospital encounters

Correlation between features and readmission

Visualization of trends

Modeling

Applied Random Forest and Logistic Regression

Evaluated using accuracy, precision, recall, F1-score, confusion matrix, and ROC-AUC

Insights & Recommendations

Highlighted the challenge of class imbalance

Suggested further techniques such as SMOTE, undersampling, cost-sensitive learning to improve minority class prediction

⚙️ Requirements

To run the notebook, install dependencies:

pip install pandas numpy matplotlib seaborn scikit-learn

▶️ Usage

Clone the repository:

git clone https://github.com/your-username/diabetes-readmission.git
cd diabetes-readmission


Open Jupyter Notebook:

jupyter notebook Main.ipynb


Run all cells step by step.

📌 Results
🔹 Random Forest

Accuracy: 0.89

Precision (Class 1 – readmitted): 0.59

Recall (Class 1 – readmitted): 0.01

ROC-AUC: 0.64

Observation: Excellent performance for majority class, but poor recall for minority class (readmitted patients).

🔹 Logistic Regression

Accuracy: 0.67

Precision (Class 1 – readmitted): 0.16

Recall (Class 1 – readmitted): 0.45

ROC-AUC: 0.60

Observation: More balanced than Random Forest, but overall weaker accuracy. Captures more readmitted patients, though at the cost of misclassifying non-readmitted cases.

⚖️ Key Challenge

The dataset’s 89:11 imbalance makes predicting readmission very difficult.

Models achieve high accuracy due to the dominance of the majority class but struggle to detect true readmissions.

Future improvements:

Class rebalancing (SMOTE, undersampling)

Ensemble methods with cost-sensitive learning

Deep learning models with weighted loss functions

📖 References

UCI Machine Learning Repository – Diabetes 130-US hospitals for readmission

Strack, B., DeShazo, J.P., Gennings, C., et al. Impact of HbA1c Measurement on Hospital Readmission Rates: Analysis of 70,000 Clinical Database Patient Records. BioMed Research International, 2014.

(By Jibran Mujtaba)