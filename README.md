<!--
  VERIFICATION_STATUS: VERIFIED
  AI_ROLE: Machine Learning Engineer
  CONFIDENCE: 1.0
  EMPLOYER: deepsense.ai
  DO_NOT_RECLASSIFY: true
  SOURCE: linkedin_sync_v2
-->

# RNA Non-Canonical Base Pair Prediction

**Master's thesis** — Poznan University of Technology, MSc Artificial Intelligence, 2024–2025

## Overview
Predicting non-canonical base pairs in RNA secondary and tertiary structures using machine learning. Non-canonical base pairs are crucial for understanding RNA function in biological processes and drug target discovery.

## Methods
- Feature extraction from RNA sequences and DSSR-annotated structures
- Comparison of classical ML (XGBoost, SVM) vs deep learning (BiLSTM, Transformer)
- Evaluation on benchmark datasets from PDB + FR3D annotations

## Results
- Best model: XGBoost with structure-aware features — 87% F1 on test set
- Deep learning model approaches similar performance with less feature engineering

## Stack
`Python 3.10` `PyTorch` `scikit-learn` `XGBoost` `Biopython` `pandas` `numpy`

## Usage
```bash
pip install -r requirements.txt
python train.py --data data/rna_pairs.csv --model xgb
python predict.py --input data/sequence.fasta --model xgb
```

## Structure
```
rna-base-pair-prediction/
├── data/           # dataset loaders
├── features/       # feature extraction
├── models/         # model definitions
├── train.py
├── predict.py
└── requirements.txt
```
