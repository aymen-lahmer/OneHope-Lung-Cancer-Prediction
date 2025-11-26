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
    * **Radiomic Module:** Uses **Fuzzy Logic** to interpret manual radiomic inputs (Entropy, Sphericity, Volume) without requiring heavy GPU infrastructure.
* **Explainable AI (XAI):** Integrated **SHAP (SHapley Additive exPlanations)** values to provide clinicians with transparent reasoning behind every prediction.
* **User-Friendly GUI:** Developed with **PySide6**, featuring patient management, visualization tabs, and report generation.
* **AI Assistant:** Includes "DILA", a voice assistant based on Llama 3 to guide users.

## 📊 Model Performance
The XGBoost model was rigorously validated using 5-fold cross-validation on the TCIA NSCLC Radiogenomics dataset.

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
* **Data Source:** [The Cancer Imaging Archive (TCIA) - NSCLC Radiogenomics](https://www.cancerimagingarchive.net/).

## 🏥 Clinical Validation
This project and its methodology have been reviewed and validated by **Dr. Rabah LAHMER**, Pneumologist (Ain M'lila, Algeria), confirming the clinical relevance of the selected features and the utility of the tool in oncological follow-up.

## 📸 Screenshots
![Page d'accueil](home.png)
<img width="1260" height="660" alt="One hope" src="https://github.com/user-attachments/assets/605840ff-4ea3-45c9-ae77-2ce8e94e58fa" />


## 👥 Authors & Acknowledgments
* **Developer:** Mohammed Aymen LAHMER (State Engineer in Biotechnology)
* **Supervisors:** Pr. Dalila NAIMI & Dr. Ahmed BOUZIANE (ENSB).
* **Medical Expert:** Dr. Rabah LAHMER.

---
*This repository contains the source code and documentation for the One Hope project.*
