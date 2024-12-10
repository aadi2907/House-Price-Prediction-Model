# Housing Price Prediction Model

This repository contains a machine learning model to predict housing prices based on various features such as area, number of bedrooms, bathrooms, and other amenities. The dataset is preprocessed and used to train a Linear Regression model.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Dataset Details](#dataset-details)
- [Data Preprocessing](#data-preprocessing)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Results](#results)
- [Setup and Usage](#setup-and-usage)
- [Contributors](#contributors)

---

## Project Overview
This project aims to predict housing prices using a dataset of real estate properties. The dataset includes various features such as:
- Area
- Number of bedrooms, bathrooms, and stories
- Parking facilities
- Whether the property has amenities like a basement, air conditioning, etc.

The final model uses **Linear Regression** to make predictions.

---

## Technologies Used
- **Programming Language**: Python
- **Libraries**: 
  - pandas
  - numpy
  - scikit-learn
  - matplotlib (optional for visualization)

---

## Dataset Details
The dataset used contains 545 entries with the following columns:
- **Numerical Columns**: `price`, `area`, `bedrooms`, `bathrooms`, `stories`, `parking`
- **Categorical Columns**: `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `prefarea`, `furnishingstatus`

The dataset was cleaned, encoded, and scaled before being used in the model.

---

## Data Preprocessing
The following preprocessing steps were applied:
1. **Binary Encoding**: Columns like `mainroad`, `guestroom`, etc., were encoded into binary (`0` for "no", `1` for "yes").
2. **One-Hot Encoding**: The `furnishingstatus` column was one-hot encoded into:
   - `furnishingstatus_furnished`
   - `furnishingstatus_semi-furnished`
   - `furnishingstatus_unfurnished`
3. **Feature Scaling**: Numerical columns were standardized using `StandardScaler` from `scikit-learn`.

---

## Model Training and Evaluation
- **Model Used**: Linear Regression
- **Train-Test Split**: The data was split into 80% training and 20% testing sets.
- **Performance Metrics**:
  - **Mean Absolute Error (MAE)**: *calculated_value*
  - **Mean Squared Error (MSE)**: *calculated_value*
  - **R-Squared (R²)**: *calculated_value*

---

## Results
The model achieved the following results:
- **MAE**: `*662889.8475037976*`
- **MSE**: `*847152968184.9515*`
- **R² Score**: `*0.704408346767002*`

---

## Setup and Usage
To use this repository, follow these steps:

### Prerequisites
Ensure Python is installed along with the following libraries:
```bash
pip install pandas numpy scikit-learn matplotlib
```
### Clone the repository
```bash
git clone https://github.com/aadi2907/House-Price-Prediction-Model.git
cd housing-price-prediction
```
### Run the code
- Load the dataset (Housing.csv).
- Preprocess the data as shown in the Data Preprocessing section.
- Train the model:
```bash
python model_training.py
```
- Predict and evaluate the results.
