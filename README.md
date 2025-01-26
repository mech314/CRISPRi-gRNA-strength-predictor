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
```

## **External Dependencies**
RNAfold (required for calculating self-folding MFE): See instructions below for installation.
Installing RNAfold

RNAfold is part of the ViennaRNA package. Follow these steps to install it on your system:

## **On Ubuntu/Debian:**
Update your package manager:
```bash
sudo apt update
```
Install the ViennaRNA package:
```bash
sudo apt install viennarna
Verify the installation:
```
```bash
RNAfold --version
```
## **On macOS:**
Install Homebrew if you don't already have it:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Use Homebrew to install ViennaRNA:
```bash
brew install viennarna
```
Verify the installation:
```bash
RNAfold --version
```
On Windows:
Download the precompiled ViennaRNA binaries from the official website.
Extract the downloaded files and add the bin folder to your system's PATH environment variable.
Verify the installation by opening a terminal and running:
```bash
RNAfold --version
```
Note:
Ensure that RNAfold is accessible from the command line after installation. If not, verify that its path has been correctly added to your system's environment variables.

# Key Features

## **Feature Engineering**

GC Content: Computes GC content for specified regions of the gRNA sequence.
- Melting Temperature: Estimates Tm using the Wallace Rule and salt-adjusted formulas. 
- Self-Folding MFE: Calculates the minimum free energy using RNAfold.
- Motif Detection: Identifies motifs such as GGGG, TTTT, and others in the sequence.
- Position-Specific Features: Examines nucleotide properties at critical positions.
- Handles class imbalance with SMOTE and SMOTE-Tomek.
- Utilizes CatBoostClassifier
- Scales features using StandardScaler and MinMaxScaler.
- Outputs feature importance for interpretability.
- Classification metrics: Accuracy, precision, recall, F1-score, and AUC.
- Confusion matrix visualization for model performance.


