# MUFG DataScience Challenge 2025

A machine learning competition focused on predicting crowdfunding project success through binary classification.

## Project Overview

This repository contains the solution for the MUFG DataScience Challenge 2025, where the goal is to predict whether a crowdfunding project will succeed (final_status = 1) or fail (final_status = 0).

## Dataset

- **train.csv**: Training data with features and target variable (final_status)
- **test.csv**: Test data without target variable (for predictions)
- **sample_submit.csv**: Sample submission format (id, prediction)
- **description.txt**: Detailed feature descriptions in Japanese

## Key Features

The dataset includes various crowdfunding project attributes:
- Project metadata: name, description, goal amount, keywords
- Temporal data: creation, launch, deadline timestamps (UNIX format)
- Geographic: country, currency
- Communication settings: disable_communication flag
- Target: final_status (1=success, 0=failure)

## Project Structure

```
├── data/
│   ├── raw/                    # Original dataset files
│   ├── processed/              # Cleaned and processed data
│   ├── features/               # Feature engineered datasets
│   └── submissions/            # Model predictions
├── notebooks/
│   ├── eda/                    # Exploratory Data Analysis
│   ├── modeling/               # Model development
│   └── experiments/            # Various experiments
├── models/
│   ├── baseline/               # Baseline models
│   ├── random_forest/          # Random Forest models
│   ├── xgboost/               # XGBoost models
│   ├── lightgbm/              # LightGBM models
│   ├── neural_networks/       # Deep learning models
│   └── ensemble/              # Ensemble methods
├── CLAUDE.md                   # AI assistant instructions
└── README.md                   # This file
```

## Development Notes

- This is a data science competition focused on binary classification
- Key considerations include temporal feature engineering, text processing (NLP), and handling class imbalance
- UNIX timestamps require conversion to datetime for temporal analysis
- Text fields (name, desc, keywords) may benefit from NLP techniques
- Currency and country fields suggest potential for geographic/economic feature engineering

## Getting Started

1. Explore the data with notebooks in `notebooks/eda/`
2. Review feature engineering approaches in `notebooks/modeling/`
3. Check baseline model performance in `models/baseline/`
4. Experiment with different algorithms in respective model directories

## Competition Format

Final predictions should follow the format specified in `sample_submit.csv`:
- id: Project identifier
- prediction: Probability of success (0-1)