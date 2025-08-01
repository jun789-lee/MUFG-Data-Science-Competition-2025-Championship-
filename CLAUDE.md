# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the MUFG DataScience Challenge 2025 dataset - a machine learning competition focused on predicting crowdfunding project success. The task is binary classification: predict whether a crowdfunding project will succeed (final_status = 1) or fail (final_status = 0).

## Dataset Structure

- **train.csv**: Training data with features and target variable (final_status)
- **test.csv**: Test data without target variable (for predictions)
- **sample_submit.csv**: Sample submission format (id, prediction)
- **description.txt**: Detailed feature descriptions in Japanese

## Key Features

The dataset includes crowdfunding project attributes:
- Project metadata: name, description, goal amount, keywords
- Temporal data: creation, launch, deadline timestamps (UNIX format)
- Geographic: country, currency
- Communication settings: disable_communication flag
- Target: final_status (1=success, 0=failure)

## Development Notes

- This is a data science competition dataset, not a code project
- No build/test commands are needed - this is purely data files
- Analysis should focus on feature engineering, model selection, and evaluation metrics appropriate for binary classification
- Temporal features (timestamps) likely require preprocessing and feature extraction
- Text features (name, desc, keywords) may benefit from NLP techniques
- Consider class imbalance when developing models
- Use sample_submit.csv format for final predictions

## Data Analysis Considerations

- UNIX timestamps need conversion to datetime for temporal analysis
- Text fields may contain special characters and require cleaning
- Currency and country fields suggest potential for geographic/economic feature engineering
- Goal amounts vary widely - consider scaling/normalization
- Missing values should be checked and handled appropriately