# Data Directory Structure

This directory contains all data files organized by purpose and processing stage.

## Folder Structure

### 📁 `raw/`
Original, unmodified competition data files:
- `train.csv` - Training dataset with target variable (final_status)
- `test.csv` - Test dataset for predictions (no target variable)
- `sample_submit.csv` - Sample submission format
- `description.txt` - Feature descriptions and data dictionary

### 📁 `processed/`
Cleaned and preprocessed data ready for modeling:
- Store cleaned datasets with consistent naming
- Example: `train_cleaned.csv`, `test_cleaned.csv`
- Include data after basic preprocessing (missing values, outliers, etc.)

### 📁 `features/`
Feature-engineered datasets with different feature sets:
- `features_v1/` - Basic temporal + text features
- `features_v2/` - Advanced NLP features
- `features_v3/` - Interaction features
- `features_v4/` - Domain-specific features
- Each version should include:
  - `X_train.csv` - Training features
  - `X_test.csv` - Test features
  - `y_train.csv` - Training targets
  - `feature_names.txt` - List of feature names

### 📁 `submissions/`
Model predictions and submission files:
- Use naming convention: `{model}_{features}_{version}_submission.csv`
- Examples:
  - `rf_basic_v1_submission.csv`
  - `xgb_advanced_v2_submission.csv`
  - `ensemble_final_submission.csv`

## Usage Guidelines

1. **Never modify files in `raw/`** - Keep original data intact
2. **Version your feature sets** - Use descriptive folder names in `features/`
3. **Document your features** - Include feature descriptions and methodology
4. **Track submissions** - Maintain clear naming for different experiments