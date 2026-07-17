# STUDENT MARKS PREDICTOR

## Overview

This project is an end-to-end Machine Learning application developed to understand how machine learning systems are built, structured, and deployed in real-world environments.

The objective is to predict a student's Mathematics score based on demographic and academic factors such as gender, race/ethnicity, parental level of education, lunch type, test preparation course, reading score, and writing score.

The primary focus of this project was understanding the complete machine learning lifecycle from data ingestion to model deployment.

---

## Project Objectives

* Understand the end-to-end machine learning workflow
* Learn industry-style project structuring
* Implement modular and reusable code
* Build data ingestion and transformation pipelines
* Train and evaluate multiple machine learning models
* Serialize models and preprocessing pipelines
* Develop a prediction pipeline
* Integrate machine learning with a Flask web application
* Gain practical experience with production-oriented ML development

---

## Features

### Data Ingestion

* Reads raw dataset
* Splits data into training and testing datasets
* Stores processed datasets for downstream components

### Data Transformation

* Handles categorical and numerical features
* Applies feature encoding and scaling
* Creates reusable preprocessing pipelines
* Saves preprocessing object as `preprocessor.pkl`

### Model Training

* Trains multiple regression models
* Compares model performance
* Selects the best-performing model
* Saves trained model as `model.pkl`

### Prediction Pipeline

* Loads trained model and preprocessing artifacts
* Transforms incoming user data
* Generates predictions in real time

### Flask Web Application

* User-friendly web interface
* Accepts student information through forms
* Processes inputs using the prediction pipeline
* Returns predicted Mathematics scores instantly

---

## Flask Web Application

The project includes a Flask-based web application that serves as the interface between users and the machine learning model.

### Role of Flask

Flask acts as the backend server responsible for:

* Receiving user inputs through HTML forms
* Processing incoming data
* Loading the saved preprocessing pipeline (`preprocessor.pkl`)
* Loading the trained machine learning model (`model.pkl`)
* Executing the prediction pipeline
* Returning predictions to the user interface

### Application Workflow

```text
User Input
     ↓
HTML Form
     ↓
Flask Application
     ↓
Prediction Pipeline
     ↓
Preprocessor
     ↓
Trained Model
     ↓
Prediction
     ↓
Web Interface
```

Using Flask allowed the machine learning model to be exposed as a web application, simulating how predictive models are integrated into software systems.

---

## Project Structure

```text
MLProjects/
│
├── artifacts/
│   ├── model.pkl
│   └── preprocessor.pkl
│
├── notebooks/
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   │
│   ├── pipeline/
│   │   └── predict_pipeline.py
│   │
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
│
├── templates/
│   ├── index.html
│   └── home.html
│
├── app.py
├── requirements.txt
├── setup.py
└── README.md
```

---

## Machine Learning Workflow

```text
Raw Dataset
      ↓
Data Ingestion
      ↓
Data Transformation
      ↓
Feature Engineering
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Model Serialization
(model.pkl + preprocessor.pkl)
      ↓
Prediction Pipeline
      ↓
Flask Application
      ↓
Prediction
```

---

## Technologies Used

### Programming Language

* Python

### Machine Learning

* Scikit-Learn
* CatBoost
* XGBoost
* Pipeline checks for best model

### Data Processing

* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn

### Backend Development

* Flask

### Model Serialization

* Pickle
* Dill

### Version Control

* Git
* GitHub

---

## Input Features

The model uses the following features:

* Gender
* Race/Ethnicity
* Parental Level of Education
* Lunch Type
* Test Preparation Course
* Reading Score
* Writing Score

### Output

* Predicted Mathematics Score

---

## Key Learnings

Through this project, I gained hands-on experience with:

* Data ingestion pipelines
* Data preprocessing and transformation
* Feature engineering
* Machine learning model training
* Model evaluation and selection
* Model serialization using Pickle
* Prediction pipelines
* Exception handling and logging
* Flask application development
* End-to-end machine learning workflows
* Project structuring and code modularization

---

## Future Work

The current version focuses on building and understanding the complete machine learning pipeline.

Future enhancements include:

* Docker containerization
* Cloud deployment
* AWS EC2 deployment
* AWS Elastic Beanstalk deployment
* AWS Elastic Container Registry (ECR)
* Azure Container Services
* CI/CD pipelines
* MLflow experiment tracking

---

## Project Significance

This project was developed primarily as a learning initiative to understand how machine learning projects are implemented beyond notebook-based experimentation.

It covers the complete lifecycle:

```text
Data Ingestion
      ↓
Data Transformation
      ↓
Model Training
      ↓
Model Serialization
      ↓
Prediction Pipeline
      ↓
Flask Application
```

This foundation provides practical exposure to industry-oriented machine learning development and prepares the project for future deployment, containerization, and MLOps integration.

---

## Author

Vaibhav Raj

B.Tech ECE Student

Data Science Enthusiast
