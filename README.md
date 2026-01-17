# Reducing Readmissions: Hospital Administration Data Analysis

## 🏥 Project Background
As a data analyst in the hospital administration department at Novartis, this project focuses on improving patient care by reducing unnecessary hospital readmissions. Recently, the hospital has experienced a spike in readmission rates, raising concerns about healthcare costs, patient outcomes, and the hospital's reputation.

The goal of this analysis is to identify patterns and factors associated with high readmission rates to drive targeted interventions and optimize resource allocation.

## 🎯 Objectives
1.  **Analyze Admission Data:** Identify underlying causes of readmissions.
2.  **Assess Demographics:** Understand how age, race, and gender impact outcomes.
3.  **Evaluate Operational Metrics:** Correlate length of stay, lab procedures, and previous visits with readmission risk.
4.  **Provide Actionable Insights:** Support stakeholders (Board, C-Suite, Clinicians) with data-driven recommendations.

## 📂 Data Dictionary
The dataset contains patient encounter data with the following key features:

| Feature | Description |
| :--- | :--- |
| `readmitted` | Target variable: 1 if readmitted <30 days, else 0  |
| `encounter_id` / `patient_id` | Unique identifiers for encounters and patients  |
| `race`, `gender`, `age` | Patient demographics  |
| `time_in_hospital` | Length of stay in days  |
| `medical_specialty` | Admitting physician's specialty  |
| `num_lab_procedures` | Number of lab tests performed  |
| `num_medications` | Number of distinct medications prescribed  |
| `number_emergency` | Emergency visits in the preceding year  |
| `diag_1` - `diag_5` | Primary and secondary diagnosis codes  |
| `diabetesMed` | Indicates if diabetic medication was prescribed  |

## 📊 Key Findings

### Basic Analysis
* **Age:** Readmission rates increase significantly with age, peaking in the 70-90 age range.
* **Prior History:** There is a strong positive correlation between the number of previous emergency visits and the likelihood of readmission.
* **Medication Complexity:** Patients with a higher number of prescribed medications tend to have longer hospital stays.
* **Diabetes:** Patients on diabetes medication show higher readmission rates compared to those not on medication.

### Medium-Level Insights
* **Comorbidities:** A higher number of diagnoses (`number_diagnoses`) is associated with both longer stays and higher readmission rates.
* **"Frequent Flyers":** Certain primary diagnoses are linked to patients with extensive histories of inpatient and emergency visits.
* **Medication Impact:** Users of specific medications often have higher readmission rates than non-users, suggesting these patients have more severe or harder-to-manage conditions.

## 🛠️ Installation & Usage

### Prerequisites
* Python 3.8+
* Jupyter Notebook

### Setup
1.  Clone the repository:
    ```bash
    git clone [https://github.com/yourusername/hospital-readmission-analysis.git](https://github.com/yourusername/hospital-readmission-analysis.git)
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Run the analysis:
    Open `notebooks/hospital_analysis.ipynb` and execute the cells to reproduce the analysis and visualizations.

## 📈 Visualizations
The analysis includes various visualizations, including:
* Readmission Rate by Age Group
* Average Length of Stay by Specialty
* Correlation Heatmaps (Race/Gender)
* Impact of Prior Emergency Visits

## 🤝 Stakeholders
This analysis addresses the needs of:
* **C-Suite:** For cost and reputation management.
* **Clinicians:** For improving treatment protocols and discharge planning.
* **Patients:** For better care quality and transparency.

## 📜 License
This project is for educational purposes as part of the Novartis Data Analytics Case Study.
