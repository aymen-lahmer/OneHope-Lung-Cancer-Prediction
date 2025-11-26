# 🎗️ One Hope: NSCLC Recurrence Prediction System

[![Python](https://img.shields.io/badge/Python-3.9-3776AB?logo=python)](https://www.python.org/)
[![XGBoost](https://img.shields.io/badge/Model-XGBoost-red)](https://xgboost.readthedocs.io/)
[![GUI](https://img.shields.io/badge/Interface-PySide6-green)](https://doc.qt.io/qtforpython/)
[![Status](https://img.shields.io/badge/Status-Completed-success)]()

> **"Le meilleur moyen de prédire l'avenir, c'est de le créer."**

## 📌 Project Overview
**One Hope** is a desktop application developed as an Engineering Graduation Project (PFE Startup) at *École Nationale Supérieure de Biotechnologie (ENSB)*. 

It serves as a **clinical decision support tool** designed to predict the risk of recurrence in patients with **Non-Small Cell Lung Cancer (NSCLC)**. The system utilizes a hybrid Artificial Intelligence approach combining Machine Learning on clinical data and Fuzzy Logic on radiomic features.

## 🚀 Key Features
* **Hybrid Prediction Engine:**
    * **Clinical Module:** Uses **XGBoost** to analyze clinical and biological data (Age, TNM Stage, Smoking history, biomarkers).
    * [cite_start]**Radiomic Module:** Uses **Fuzzy Logic** to interpret manual radiomic inputs (Entropy, Sphericity, Volume) without requiring heavy GPU infrastructure[cite: 37].
* [cite_start]**Explainable AI (XAI):** Integrated **SHAP (SHapley Additive exPlanations)** values to provide clinicians with transparent reasoning behind every prediction[cite: 1073].
* **User-Friendly GUI:** Developed with **PySide6**, featuring patient management, visualization tabs, and report generation.
* [cite_start]**AI Assistant:** Includes "DILA", a voice assistant based on Llama 3 to guide users[cite: 854].

## 📊 Model Performance
[cite_start]The XGBoost model was rigorously validated using 5-fold cross-validation on the TCIA NSCLC Radiogenomics dataset[cite: 954].

| Metric | Score (Mean ± SD) |
| :--- | :--- |
| **Accuracy** | **82.1%** (± 4.1%) |
| **AUC** | **0.898** (± 2.4%) |
| **Precision**| 81.8% |
| **Recall** | 82.7% |
| **F1-Score** | 82.0% |

## 🛠️ Tech Stack
* **Core Language:** Python 3.9
* **GUI Framework:** PySide6 (Qt)
* **Machine Learning:** XGBoost, Scikit-learn, Pandas, NumPy.
* **Explainability:** SHAP.
* [cite_start]**Data Source:** [The Cancer Imaging Archive (TCIA) - NSCLC Radiogenomics](https://www.cancerimagingarchive.net/)[cite: 691].

## 🏥 Clinical Validation
This project and its methodology have been reviewed and validated by **Dr. [cite_start]Rabah LAHMER**, Pneumologist (Ain M'lila, Algeria), confirming the clinical relevance of the selected features and the utility of the tool in oncological follow-up[cite: 886].

## 📸 Screenshots
*(Placeholder for screenshots of the One Hope Interface, e.g., Home Tab, Prediction Report, SHAP Graphs)*

## 👥 Authors & Acknowledgments
* **Developer:** Mohammed Aymen LAHMER (State Engineer in Biotechnology)
* **Supervisors:** Pr. Dalila NAIMI & Dr. Ahmed BOUZIANE (ENSB).
* **Medical Expert:** Dr. Rabah LAHMER.

---
*This repository contains the source code and documentation for the One Hope project.*
