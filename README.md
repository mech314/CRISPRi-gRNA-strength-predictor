 CRISPRi gRNA Strength Predictor

This repository focuses on predicting the strength of CRISPR interference (CRISPRi)-mediated gene repression using machine learning techniques. By leveraging features from recent literature, such as gRNA sequences and their proximity to the PAM site, this project aims to train a classification model to identify key factors influencing repression strength. Additionally, it explores inconsistencies in reported data to provide insights into contradictory findings and enhance our understanding of the determinants of CRISPRi effectiveness.

## Features

- **Data Analysis**: Examination of gRNA sequences and their associated features.
- **Machine Learning Model**: Training of a classification model to predict gRNA repression strength.
- **Inconsistency Exploration**: Analysis of discrepancies in reported data to uncover potential contradictions.

## Requirements

To run the analyses and models in this repository, ensure you have the following installed:

- **Python** (version 3.6 or higher)
- **Jupyter Notebook**

### Python Packages

Install the required Python packages using `pip`:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
