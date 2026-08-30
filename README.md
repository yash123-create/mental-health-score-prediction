# Mental Health Score Prediction

A machine learning-based web application that predicts a student's mental health score using academic, lifestyle, and social media-related factors.

## Overview

Mental health can be influenced by several aspects of a student's daily life, including social media usage, sleep, physical activity, academic workload, stress, and study patterns.

This project uses machine learning to analyze these factors and estimate a student's mental health score. The trained model is integrated into a web application where users can enter relevant information and receive a predicted score.

## Objectives

- Analyze factors associated with student mental health.
- Perform data preprocessing and exploratory data analysis.
- Develop a machine learning regression model for mental health score prediction.
- Evaluate model performance using appropriate regression metrics.
- Save the trained model for application-level predictions.
- Integrate the machine learning model with a web-based interface.

## Dataset

The project uses the following dataset:

**Student Social Media And Mental Health Impact.csv**

The dataset contains student-related information covering demographic, academic, lifestyle, and social media usage factors.

Important input attributes include:

- Age
- Gender
- Country
- Academic Level
- Social Media Platform
- Primary Purpose of Social Media Use
- Daily Social Media Usage
- Daily Social Media Unlocks
- Study Hours
- Physical Activity
- Sleep Hours
- Stress Level

The target variable is:

**Mental_Health_Score**

## Machine Learning Approach

The project treats mental health score prediction as a **regression problem** because the target value is a continuous numerical score.

The machine learning workflow includes:

1. Loading the dataset
2. Inspecting and understanding the data
3. Data cleaning and preprocessing
4. Exploratory data analysis
5. Preparing input features and target variable
6. Splitting the dataset into training and testing sets
7. Applying feature preprocessing
8. Training regression models
9. Comparing model performance
10. Hyperparameter tuning
11. Selecting the final model
12. Saving the trained model using Joblib

### Preprocessing

Different preprocessing techniques are applied according to the type of feature.

- Numerical features are scaled using `StandardScaler`.
- Categorical features are transformed using encoding techniques.
- A `ColumnTransformer` is used to organize the preprocessing workflow.

### Model

The final prediction pipeline uses:

**Random Forest Regressor**

Hyperparameter tuning is performed using `RandomizedSearchCV` to improve model performance.

### Evaluation Metrics

The model is evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

These metrics are used to assess how accurately the model predicts the mental health score.

## Web Application

The trained machine learning pipeline is integrated into a web application.

The application allows a user to provide the required student information through a web interface. The submitted data is sent to the backend, processed using the same preprocessing pipeline used during training, and passed to the trained model.

The application then returns the predicted mental health score.

## Project Architecture

    User Input
        |
        v
    Web Interface
    (HTML / CSS / JavaScript)
        |
        v
    FastAPI Backend
        |
        v
    Input Validation
        |
        v
    Saved ML Pipeline
        |
        v
    Random Forest Regressor
        |
        v
    Predicted Mental Health Score

## Technologies Used

### Programming & Machine Learning

- Python
- Pandas
- NumPy
- Scikit-learn
- Joblib

### Backend

- FastAPI
- Pydantic
- Uvicorn

### Frontend

- HTML
- CSS
- JavaScript

### Development

- Jupyter Notebook
- Git
- GitHub

## Project Structure

    mental-health-score-prediction/
    |
    ├── ML_Project.ipynb
    ├── Mental_Health_Model.pkl
    ├── Student Social Media And Mental Health Impact.csv
    |
    ├── main.py
    ├── requirements.txt
    |
    ├── index.html
    ├── script.js
    ├── style.css
    |
    ├── ML Project.html
    └── README.md

## Running the Project Locally

### 1. Clone the repository

    git clone https://github.com/yash123-create/mental-health-score-prediction.git

### 2. Navigate to the project directory

    cd mental-health-score-prediction

### 3. Install the required dependencies

    pip install -r requirements.txt

### 4. Start the backend

    uvicorn main:app --reload

### 5. Open the web application

Open the frontend in a browser and use the prediction interface to enter the required student information.

## Model Workflow

The complete machine learning workflow follows these stages:

    Student Dataset
          |
          v
    Data Analysis
          |
          v
    Data Preprocessing
          |
          v
    Feature Transformation
          |
          v
    Train/Test Split
          |
          v
    Model Training
          |
          v
    Hyperparameter Tuning
          |
          v
    Model Evaluation
          |
          v
    Saved Model (.pkl)
          |
          v
    Web Application
          |
          v
    Mental Health Score Prediction

## Key Features

- Machine learning-based mental health score prediction
- Numerical and categorical feature preprocessing
- Random Forest regression
- Hyperparameter optimization
- Saved trained model pipeline
- REST API backend
- Interactive web interface
- End-to-end machine learning workflow

## Future Improvements

- Deploy the application as a cloud-hosted service.
- Add additional student wellness and behavioral indicators.
- Improve model performance using additional algorithms and ensemble techniques.
- Add visualization of prediction-related factors.
- Provide a more detailed analytics dashboard.
- Continuously retrain the model with additional relevant data.

## Disclaimer

This project is intended for educational and machine learning demonstration purposes. The predicted score should not be considered a medical diagnosis or professional mental health assessment.

## Author

**Yash Mehra**

GitHub:

https://github.com/yash123-create
