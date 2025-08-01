# Models Directory Structure

This directory contains trained models, configurations, and results organized by algorithm type.

## Folder Structure

### 📁 `baseline/`
Simple baseline models for comparison:
- Basic feature sets with standard algorithms
- Minimal hyperparameter tuning
- Quick performance benchmarks

### 📁 `random_forest/`
Random Forest models and experiments:
- Different hyperparameter configurations
- Feature importance analysis
- Cross-validation results
- Model files: `rf_model_v{X}.pkl`

### 📁 `xgboost/`
XGBoost models and experiments:
- Hyperparameter tuning results
- Feature importance plots
- Learning curves
- Model files: `xgb_model_v{X}.pkl`

### 📁 `lightgbm/`
LightGBM models and experiments:
- LGBM-specific configurations
- Fast training experiments
- Model files: `lgb_model_v{X}.pkl`

### 📁 `neural_networks/`
Deep learning models:
- Neural network architectures
- Training histories
- Model checkpoints
- Model files: `nn_model_v{X}.h5` or `.pth`

### 📁 `ensemble/`
Ensemble methods and model combinations:
- Voting classifiers
- Stacking models
- Blending experiments
- Meta-learner configurations

## File Naming Conventions

### Model Files
- Format: `{algorithm}_model_{features}_{version}.{ext}`
- Examples:
  - `rf_model_basic_v1.pkl`
  - `xgb_model_advanced_v2.pkl`
  - `ensemble_final_v1.pkl`

### Configuration Files
- Format: `{algorithm}_config_{version}.json`
- Store hyperparameters, training settings

### Results Files
- Format: `{algorithm}_results_{version}.json`
- Store metrics, validation scores, timestamps

## Usage Guidelines

1. **Version everything** - Use clear versioning for iterative improvements
2. **Document experiments** - Include configuration and results files
3. **Save trained models** - Store models for reproducibility and ensemble building
4. **Track performance** - Maintain results files with metrics and timestamps
5. **Use consistent naming** - Follow the established naming conventions