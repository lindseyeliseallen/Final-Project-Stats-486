# Data Directory

## Primary Dataset

**Name:** Diabetes 130-US Hospitals Dataset  
**Source:** UCI Machine Learning Repository  
**Link:** https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008  

### Description
This dataset contains over 100,000 hospital records for diabetic patients across 130 U.S. hospitals between 1999 and 2008. It includes patient demographics, diagnoses, medications, and hospital outcomes.

### Target Variable
- `readmitted`: Indicates whether a patient was readmitted within 30 days, after 30 days, or not readmitted  
- For this project, we will convert this into a binary variable (readmitted within 30 days vs not)

### Planned Features
Examples of features we plan to use:
- Age
- Gender
- Number of diagnoses
- Time in hospital
- Number of medications
- Admission type

---

## Backup Dataset

**Name:** Heart Disease Dataset  
**Source:** UCI Machine Learning Repository  
**Link:** https://archive.ics.uci.edu/ml/datasets/heart+disease  

### Description
This dataset contains patient clinical features used to predict the presence of heart disease.

### Target Variable
- Presence of heart disease (binary classification)

## Project Structure & Reproducibility

### Repository Organization
The repository is organized to ensure a clean, reproducible workflow:
1. **data:** Contains the README file and primary datasets, such as diabetic_data.csv and IDS_mapping.csv.

2. **notebooks:** Contains the core analytical code:
* eda_project2 (2).ipynb: Initial data exploration and visualization.
* supervised_models.ipynb: Training and evaluation of Random Forest and Logistic Regression models.
* UNSUPERVISED (2).ipynb: Implementation of K-Means clustering and PCA.

3. **progress:** Contains the formal written reports and embedded analysis:
* 01_proposal.md
* 02_eda.md
* 03_supervised_model.md
* 04_unsupervised_model.md.

### Exact Run Order

To reproduce the findings and plots shown in the reports, execute the notebooks in this sequence:
1. **notebooks/eda_project2 (2).ipynb**: Run first to understand the data distribution and cleaning steps.

2. **notebooks/supervised_models.ipynb**: Run to generate the feature importance rankings and baseline classification results.

3. **notebooks/UNSUPERVISED (2).ipynb**: Run to perform the final clustering and dimensionality reduction.

Technical Note: Within this notebook, the Silhouette Score is calculated using a random sample of 5,000 rows. This choice ensures the notebook runs efficiently on large-scale data while maintaining statistical validity for the cluster validation.

### Demo Artifact: Patient Mapping Results

The primary demo artifact for this project is the notebooks/UNSUPERVISED (2).ipynb file.

- What it shows: The notebook is saved with all outputs active, including the final patient mapping table.

- Key Insight: This patient mapping demonstrates that Cluster 2 represents the highest-risk group. These patients are characterized by the highest medical complexity (average of 7.65 diagnoses) and the longest hospital stays (4.59 days). This identifies a specific clinical profile that drives 30-day readmission risk.

### How to Reproduce

1.  Ensure the following libraries are installed: pandas, numpy, scikit-learn, matplotlib, seaborn, scipy, and IPython.

3. Verify the dataset files are located in the data/folder.
Note: If running in Google Colab, ensure data files are uploaded to the /sample_data/ directory to match the notebook paths.

5. Open the notebooks in the Exact Run Order listed above and execute all cells.

---
