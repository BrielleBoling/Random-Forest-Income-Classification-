# Random-Forest-Income-Classification-

Predicting **Education Level** (HS, BS, MBA, PHD) from demographic and lifestyle factors using Random Forests.

> This repository packages a project for building and evaluating Random Forest models, including data exploration, model training, and comparative evaluation between a 100-tree and a 500-tree configuration.

## Dataset
- **Name:** `Income2.csv` (210 observations, 10 columns)
- **Target:** `Education` (HS, BS, MBA, PHD)
- **Selected predictors:** Experience, GPA, Age, Income, CreditScore, NoCars, ParkingTickets, NewestCarYear, NumberKids.

## What’s Implemented
- Data profiling and sanity checks
- Optional bootstrapping to 10,000 samples (with replacement)
- **Model A:** RandomForest (100 trees, Gini)
- **Model B:** RandomForest (500 trees, Gini, train/test split, dummy encoding)
- Metrics: accuracy, precision, recall, F1-score, confusion matrices
- Side-by-side comparison and model selection

## Results Summary

After running both models, the following results were observed:

| Model | Trees | Accuracy | Precision | Recall | F1-score | Notes |
|-------|-------|----------|-----------|--------|----------|-------|
| 1     | 100   | 100%      | 100%       | 100%    | 100%      | Simpler model, uses bagging | 
| 2     | 500   | 100%      | 100%       | 100%    | 100%      | Uses dummy variables and train/test split |

**Key Findings:**
- Both models achieved perfect scores across all five evaluation metrics.
- Model 1 (100 trees with bagging) is preferred for deployment due to requiring less computational power, making it cheaper to run while maintaining identical performance.
- Model 2 is equally accurate but more resource-intensive due to the higher number of trees and additional preprocessing steps.
