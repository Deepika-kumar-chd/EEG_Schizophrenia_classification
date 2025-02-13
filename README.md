# Schizophrenia Classification Using Resting-State EEG and Machine Learning
This project aims to classify Schizophrenia (SCZ) patients and healthy controls (HC) using resting-state EEG (rsEEG) signals. The pipeline involves preprocessing EEG data, extracting relevant features, and applying multiple machine learning models to compare their classification performance.

---

## Workflow
The project follows these major steps:
-EEG Preprocessing – Cleaning EEG signals using filtering and artifact removal techniques.
-Feature Extraction – Computing frequency-domain and connectivity-based features.
-Model Training & Evaluation – Using various ML models to classify schizophrenia vs. healthy controls.
-Performance Comparison – Evaluating models using metrics such as Precision, F1-score, recall and confusion matrix.
  
---

## Dataset
- **Source**: https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0188629
- **Description**: The EEG dataset consists of resting-state recordings from both Schizophrenia patients and healthy controls.Fifteen minutes of EEG data were recorded in all subjects during an eyes-closed resting state condition. Data were acquired with the sampling frequency of 250 Hz using the standard 10–20 EEG montage with 19 EEG channels: Fp1, Fp2, F7, F3, Fz, F4, F8, T3, C3, Cz, C4, T4, T5, P3, Pz, P4, T6, O1, O2.
- **Structure**:
  - Total 28 files with .edf format
    -14 Schizophrenia
    -14 Healthy Control
    
---

## Preprocessing
-Filtering: bandpass filtering (0.5-45 Hz) to remove unwanted noise like low-frequency drift or high-frequency noise.
-Re-referencing: average re-referencing method
-ICA: ICA to decompose the data and remove any independent components that correspond to artifacts (e.g., ECG, EMG, eye movements).
-Epoching: Segment the continuous data into epochs.
-Autoreject: Autoreject to remove any remaining bad epochs.
  
---

## Feature Extraction
The following features were extracted from EEG signals:
-Frequency-Domain Features: Gamma Power and Relative Gamma Power.
-Connectivity Measures: Connectivity,Phase-Locking Value (PLV) and Coherence.
  
---

## Machine Learning Models
The extracted features were used to train and evaluate the following models:
-Logistic Regression (LR)
-k-Nearest Neighbors (k-NN)
-Decision Tree (DT)
-Random Forest Classifier (RF)
-Support Vector Machine (SVM)  
Each model was optimized using Grid Search with cross-validation.

---

## Results & Performance Comparison
The models were evaluated using:
-Precision.
-Recall
-F1-score
-Accuracy

Model	Precision	Recall	F1-Score	Accuracy
Logistic Regression	0.61	0.61	0.61	0.61
K-Nearest Neighbors	0.60	0.60	0.60	0.60
Decision Tree	0.55	0.55	0.55	0.55
Random Forest	0.57	0.57	0.57	0.57
Support Vector Machine	0.64	0.64	0.64	0.64
 
---

## Key Findings: 
-Support Vector Machine model achieved the highest performance in classification.
-Decision Tree has the lowest accuracy at 0.55
