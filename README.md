# CRISPRi gRNA Strength Predictor

This repository provides a comprehensive framework for predicting the strength of gRNAs in CRISPR interference (CRISPRi) experiments. By engineering features from gRNA sequences and catboost classification and regression models, this pipeline predicts the effectiveness of gRNA-mediated repression.

## **Pipeline Overview**
The pipeline includes the following steps:
1. Data preprocessing and merging multiple input datasets.
2. Feature engineering from gRNA sequences, including:
   - GC content computation.
   - Melting temperature calculation.
   - Self-folding minimum free energy (MFE) estimation.
   - Detection of specific sequence motifs.
   - Position-specific and nucleotide count features.
3. Handling class imbalance using SMOTE and SMOTE-Tomek.
4. Training and evaluation of machine learning models (e.g., CatBoost, SVC).
5. Evaluation the model using accuracy, precision, recall, and AUC.

## **Requirements**
The pipeline is implemented in Python and requires the following dependencies:

### **Python Dependencies**
- `numpy`
- `pandas`
- `subprocess`
- `seaborn`
- `matplotlib`
- `scikit-learn`
- `imbalanced-learn`
- `catboost`

#### Install Python packages via pip:
```bash
pip install numpy pandas seaborn matplotlib scikit-learn imbalanced-learn catboost
