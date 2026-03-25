# A Comparative Machine Learning Framework for Binary Bioactivity Classification of Drug-Like Compounds

---

## 📌 Publication

This work is published in IEEE Xplore:

**Title:** A Comparative Machine Learning Framework for Binary Bioactivity Classification of Drug-Like Compounds
**Conference:** ICAICCIT 2025
**Publisher:** IEEE

🔗 https://ieeexplore.ieee.org/document/11434119

---

## ⚠️ Important Note

This project was originally developed using Google Colab.
Some file paths in the notebooks may reference local or Google Drive directories.

After cloning the repository, please update all file paths to match your local project structure.

---

## 📖 Abstract

This project addresses the problem of binary classification of drug-like compounds based on bioactivity data. The dataset is obtained from the ChEMBL database and includes molecular structures (SMILES) and IC50 values.

The workflow consists of data preprocessing, normalization, descriptor generation, and model training. Multiple machine learning and deep learning models are evaluated, including Support Vector Machine (SVM), Random Forest (RF), Decision Tree (DT), K-Nearest Neighbors (KNN), Convolutional Neural Networks (CNN), and Spiking Neural Networks (SNN).

The results demonstrate that classical machine learning models such as SVM and KNN achieve higher performance (≈90% accuracy) compared to deep learning approaches under the given dataset and feature engineering setup.

---

## 🎯 Objective

* Perform binary classification of drug-like compounds (active vs inactive)
* Evaluate multiple machine learning and deep learning models
* Compare model performance based on standard evaluation metrics

---

## ⚙️ Methodology

### 1. Data Collection

* Source: ChEMBL database
* Data includes:

  * SMILES strings
  * IC50 values

---

### 2. Preprocessing

* Removal of invalid or missing entries
* Conversion of IC50 values into categorical classes:

  * Active: IC50 ≤ 1000
  * Inactive: IC50 ≥ 10000
  * Moderate class removed

---

### 3. Feature Engineering

* Lipinski descriptors:

  * Molecular Weight (MW)
  * LogP
  * Hydrogen bond donors
  * Hydrogen bond acceptors

---

### 4. Transformation and Normalization

* Conversion: IC50 → pIC50
* Log transformation applied to reduce skewness
* Normalization applied to improve model performance

---

### 5. Descriptor Generation

* Tool: PaDEL
* Output:

  * Molecular fingerprints (~300 features)

---

### 6. Model Training and Evaluation

The following models are implemented and evaluated:

* Random Forest (RF)
* Support Vector Machine (SVM)
* Decision Tree (DT)
* K-Nearest Neighbors (KNN)
* Convolutional Neural Network (CNN)
* Spiking Neural Network (SNN)

Evaluation metrics:

* Accuracy
* Precision
* Recall
* F1 Score

---

## 📊 Results

| Model                        | Accuracy (%) | Precision | Recall | F1 Score |
| ---------------------------- | ------------ | --------- | ------ | -------- |
| Random Forest                | 88.89        | 0.89      | 0.89   | 0.89     |
| Support Vector Machine       | 90.74        | 0.91      | 0.91   | 0.91     |
| Decision Tree                | 88.89        | 0.89      | 0.89   | 0.89     |
| K-Nearest Neighbors          | 90.74        | 0.91      | 0.91   | 0.91     |
| Convolutional Neural Network | 77.78        | 0.78      | 0.78   | 0.78     |
| Spiking Neural Network       | 46.30        | 0.46      | 0.46   | 0.46     |

---

## 📌 Observations

* Classical machine learning models (SVM, KNN) demonstrate superior performance
* Deep learning models (CNN, SNN) show comparatively lower accuracy under the given dataset size
* Feature engineering significantly influences model performance
* SNN requires further optimization and larger datasets for improved results

---

## 📂 Project Structure

```id="p3ytkn"
drug-bioactivity-classification/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── final/
│       └── classification_model_data.csv
│
├── notebooks/
│   ├── 1) ChEMBL_Data_Preprocessing.ipynb
│   ├── 2) EDA_Normalization.ipynb
│   ├── 3) PaDEL_Descriptors_Calculation.ipynb
│   └── 4) RF_SVM_CNN_DT_KNN_SNN.ipynb
│
├── requirements.txt
└── README.md
```

---

## 🛠️ Requirements

```id="wtr4sd"
pandas
numpy
matplotlib
seaborn
scikit-learn
rdkit
padelpy
torch
spikingjelly
scipy
```

---

## 🚀 Execution Steps

1. Clone the repository
2. Install dependencies using `requirements.txt`
3. Execute notebooks sequentially:

   * 1. Data Preprocessing
   * 2. EDA and Normalization
   * 3. Descriptor Generation
   * 4. Model Training and Evaluation

---

## 📌 Conclusion

This study establishes a comparative framework for binary bioactivity classification and demonstrates that classical machine learning models can outperform deep learning approaches in scenarios with structured features and limited data. The results provide practical insights for model selection in computational drug discovery.

---

## 📚 Reference

Refer to the IEEE publication for detailed methodology and discussion:
https://ieeexplore.ieee.org/document/11434119
