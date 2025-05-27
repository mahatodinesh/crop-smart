# 🌾 Soil-Based Crop Prediction

## Objective
This project aims to assist farmers in selecting the most suitable crop for their field based on essential soil metrics. By predicting the optimal crop from soil features like nitrogen (N), phosphorous (P), potassium (K), and pH, we help maximize agricultural yield and reduce the cost of unnecessary testing.

## Problem Statement
Measuring all essential soil metrics can be costly and time-consuming. With limited resources, farmers need guidance on:
1. Predicting the best crop to plant based on soil conditions.
2. Identifying the most predictive soil feature to prioritize in measurements.

## Dataset
The dataset used is `soil_measures.csv` and contains:
- `N`: Nitrogen content ratio
- `P`: Phosphorous content ratio
- `K`: Potassium content ratio
- `ph`: pH value of the soil
- `crop`: Target variable (optimal crop for given conditions)

Each row represents soil metrics from a field and the crop that performs best under those conditions.

## Approach
1. **Preprocessing**
   - Loaded the dataset and checked for missing values.
   - Split data into features (`X`) and target (`y`).

2. **Modeling**
   - Used multinomial logistic regression to predict the crop.
   - Trained a separate model for each individual soil feature (`N`, `P`, `K`, `ph`).
   - Evaluated each model using the **weighted F1-score**.

3. **Evaluation**
   - Compared performance of each model based on the F1-score.
   - Identified the single most predictive soil feature for crop classification.

## Results
The feature-wise model performances (F1-score):
- Nitrogen (`N`) → *score printed*
- Phosphorous (`P`) → *score printed*
- Potassium (`K`) → **Highest F1-score**
- pH (`ph`) → *score printed*

✅ **Potassium (`K`) was found to be the most predictive feature** for identifying the best crop based on soil conditions.

## Requirements
- Python 3.7+
- pandas
- scikit-learn

Install required packages:
```bash
pip install pandas scikit-learn
