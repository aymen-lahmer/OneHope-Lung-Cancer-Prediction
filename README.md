# 🎗️ One Hope: NSCLC Recurrence Prediction System

[![Python](https://img.shields.io/badge/Python-3.9-3776AB?logo=python)](https://www.python.org/)
[![XGBoost](https://img.shields.io/badge/Model-XGBoost-red)](https://xgboost.readthedocs.io/)
[![GUI](https://img.shields.io/badge/Interface-PySide6-green)](https://doc.qt.io/qtforpython/)
[![Status](https://img.shields.io/badge/Status-Completed-success)]()

> **"Le meilleur moyen de prédire l'avenir, c'est de le créer."**

---

### ⚠️ Proprietary Software Notice
> **This repository serves as a technical showcase and documentation.**
>
> Due to **intellectual property rights** and ongoing commercial valorization within the **ENSB Incubator**, the full source code is currently **private**.
>
> *Recruiters & Partners:* I am available to provide a **live demonstration** of the software or discuss the code architecture during an interview.

---

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

## 📂 System Architecture
The project follows a modular architecture separating the GUI (View), the Logic (Model), and the Data (Controller).

```text
OneHope-App/
├── data/
│   ├── raw/                   # Raw TCIA datasets
│   └── processed/             # Cleaned data for XGBoost
├── models/
│   ├── xgboost_model.json     # Trained Model weights
│   └── scaler.pkl             # Data normalization parameters
├── src/
│   ├── main.py                # Application Entry Point
│   ├── gui/                   # PySide6 UI Components
│   ├── logic/                 # Core Algorithms
│   │   ├── model_inference.py # XGBoost Prediction Logic
│   │   ├── fuzzy_engine.py    # Fuzzy Logic Rules implementation
│   │   └── shap_explainer.py  # XAI Integration
│   └── utils/                 # PDF Generation & Tools
├── assets/                    # Icons and Images
└── requirements.txt           # Dependencies


## 🔄 Workflow Diagram
This flowchart illustrates the hybrid decision-making process implemented in the application.

```mermaid
graph TD
    A[User Input] --> B{Data Type?}
    B -- Clinical Data --> C[Data Preprocessing]
    C --> D[XGBoost Model]
    D --> E[Clinical Risk Probability]
    
    B -- Radiomic Features --> F[Fuzzification]
    F --> G[Fuzzy Inference Engine]
    G --> H[Radiomic Risk Score]
    
    E --> I[Fusion Module]
    H --> I
    I --> J[Final Recurrence Prediction]
    J --> K[SHAP Explanation & PDF Report]
