# thesis-code
M.Sc. thesis code: Anomaly detection and identification of waybills suspected of violation in cargo transportation companies using data mining of transportation documents in Yazd Province.

# Anomaly Detection and Identification of Waybills Suspected of Violation
### Using Data Mining of Transportation Documents in Yazd Province

This repository contains the implementation code and analysis scripts for my M.Sc. thesis in Information Technology (Advanced Systems).

**Author:** Mohsen Mirjalili
**Supervisor:** Dr. Seyyed Mohammad Mehdi Hosseini
**University:** Islamic Azad University, Electronic Branch
**Date:** November 2026

---

## 📋 Abstract

The potential misuse of national identification numbers in the issuance of electronic waybills can lead to unconventional activities and impose significant regulatory challenges. Given the absence of reliable fraud labels, detecting such patterns requires methods capable of identifying anomalous behaviors without relying on labeled data.

This study aims to identify and prioritize national IDs exhibiting anomalous behavioral patterns based on electronic waybills registered in Yazd province, utilizing the **Isolation Forest** algorithm. Following data preprocessing, a behavioral profile was constructed for each national ID. Seven features—including cargo entropy, destination entropy, shipper diversity, cargo-destination combination diversity, and the ratio of records—were extracted and standardized.

The final model configuration (500 trees, max_samples=0.75, max_features=1.0) achieved an average Jaccard coefficient of **0.921** across the top 1%, 5%, and 10% rankings, demonstrating high ranking stability. Out of 3,008 examined national IDs, **151** were classified as anomalous. These results do not confirm actual violations but serve as a prioritized list for expert review and targeted regulatory oversight.

---

## 🎯 Objectives

- **Data Preparation:** Clean and preprocess electronic waybill records from Yazd province (Year 1402).
- **Feature Engineering:** Extract and standardize 7 behavioral features for each unique national ID.
- **Anomaly Detection:** Implement the Isolation Forest algorithm to identify unusual behavioral patterns.
- **Parameter Tuning:** Optimize hyperparameters based on ranking stability and anomaly score separation.
- **Prioritization:** Rank national IDs based on their anomaly scores to assist regulatory inspections.

---

## 📁 Repository Structure

```text
.
├── data/                  # Data description or anonymized sample data
├── notebooks/             # Jupyter Notebooks for data exploration and visualization
├── src/
│   ├── preprocessing.py   # Data cleaning and behavioral profile extraction
│   ├── features.py        # Calculation of Entropy, Diversity, and Ratio features
│   ├── model.py           # Isolation Forest implementation and hyperparameter tuning
│   └── evaluation.py      # Stability analysis (Jaccard index) and visualizations
├── results/               # Generated plots (Correlation matrix, Boxplots, Anomaly Score distribution)
├── requirements.txt       # Python dependencies
└── README.md
