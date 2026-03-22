# Project Proposal: Predicting Hospital Readmission Risk

## AI-Generated Project Ideas

### Idea 1: Predict Hospital Readmission Risk
Use patient hospital records to predict whether a patient will be readmitted within 30 days (classification). Apply clustering to identify different patient risk groups and patterns.

### Idea 2: Heart Disease Prediction and Patient Clustering
Use clinical features to predict heart disease (classification) and apply clustering or PCA to identify subgroups of patients with similar health profiles.

### Idea 3: Predict Length of Hospital Stay
Use patient and treatment features to predict hospital stay duration (regression) and apply anomaly detection to identify unusually long or short stays.

---

## AI Reflection

We used generative AI to brainstorm healthcare-related project ideas that combine the requirements of supervised learning with an additional machine learning method. AI helped us find out where we could get an applicable dataset for our possible questions. We refined the ideas by having AI help us make sure the projects we were interested in would be manageable within the 4–5 week timeline and do not require excessive computation. We decided to go with the hospital readmission problem because it has a clear impact, available dataset, and supports both classification and clustering analysis. AI also helped us make sure that our project meets all assignment requirements.

---

## AI Interaction Excerpt

Prompt:
"We are considering predicting hospital readmission using medical data. How can we refine this idea to make it more realistic but still meaningful for a 4–5 week project?"

Response:
"To keep the project manageable, focus on a binary classification problem such as predicting 30-day readmission instead of a more complex outcome. Use a well-known dataset like the UCI diabetes dataset to avoid time spent on data collection. For additional insight, incorporate a simple clustering method (e.g., k-means) to identify patient subgroups rather than implementing more complex models."


---

## Final Research Question

Can we accurately predict whether a patient will be readmitted within 30 days, and what patient groups are most at risk based on clustering analysis?

---

## Target Variable

- Target variable: `readmitted` (binary: readmitted within 30 days vs not)

---

## Dataset Choice and Backup

### Primary Dataset
- UCI Diabetes 130-US hospitals dataset
- Contains patient demographics, diagnoses, medications, and hospital outcomes

### Backup Dataset
- UCI Heart Disease dataset
- Contains patient clinical features and heart disease diagnosis

---

## Feasibility

This project is feasible within the 4–5 week timeline because the dataset is publicly available, well-documented, and does not require large-scale computation. We will use models such as logistic regression, decision trees, and random forests, like we have already practiced on our labs. Clustering methods such as k-means are also computationally not too time-consuming. The narrow scope allows us to focus on interpretation and model comparison rather than excessive model complexity.

---

## Ethical and Legal Considerations

The dataset is publicly available and already anonamous. However, we will need to be cautious when interpreting results, because healthcare data may reflect biases (like possible demographic disparities). We will avoid making clinical recommendations and will clearly state the limitations of our models.

---

## Planned Additional ML Methods

In addition to supervised learning models (logistic regression, decision tree, and random forest), we plan to implement clustering (k-means or hierarchical clustering) to identify patient subgroups. This will help us understand patterns in the data beyond prediction and see additional insights into patient risks.