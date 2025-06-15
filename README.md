# 🔥 Calories Burnt Prediction

This project focuses on building a machine learning model to predict the number of calories burnt during various physical activities. The model is developed using Python and several popular libraries for data manipulation, analysis, and machine learning.

---

## 📑 Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Requirements](#requirements)
- [Results](#results)
- [Usage](#usage)

---

## 🧠 Project Overview

The goal of this project is to accurately estimate calorie expenditure based on an individual's physical attributes and exercise parameters. This predictive model can be useful for:

- Fitness tracking applications  
- Personalized workout recommendations  
- Health monitoring systems  

The core of the solution involves an **XGBoost Regressor** model for precise predictions.

---

## 📊 Dataset

The project utilizes two primary datasets, which are merged to create a comprehensive dataset:

### `exercise.csv`
Contains detailed exercise session data:

- `User_ID`: Unique identifier for each user  
- `Gender`: Gender of the user  
- `Age`: Age in years  
- `Height`: Height in cm  
- `Weight`: Weight in kg  
- `Duration`: Exercise duration in minutes  
- `Heart_Rate`: Avg heart rate during exercise  
- `Body_Temp`: Body temperature post-exercise  

### `calories.csv`
Contains calorie burn information:

- `User_ID`: Unique identifier  
- `Calories`: Total calories burnt  

These two files are joined using the `User_ID` column.

---

## ⚙️ Methodology

Outlined in the `Calories Burnt Prediction.ipynb` notebook, the steps include:

1. **Environment Setup**  
   Installation of required libraries like `xgboost`.

2. **Library Imports**  
   Libraries used:
   - `numpy`, `pandas`, `matplotlib`, `seaborn`
   - `sklearn.model_selection` for data splitting  
   - `xgboost` for the regression model  
   - `sklearn.metrics` for model evaluation  

3. **Data Loading**  
   Load both `.csv` files into pandas DataFrames.

4. **Data Merging**  
   Merge datasets on `User_ID`.

5. **Data Preprocessing**  
   Handle missing values, encode categorical variables, and split into training/testing sets.

6. **Model Training**  
   Train an `XGBRegressor` on the training data.

7. **Model Evaluation**  
   Evaluate using **Mean Absolute Error (MAE)**.

---

## 🧰 Requirements

Install the following Python libraries:

```bash
pip install xgboost numpy pandas matplotlib seaborn scikit-learn
