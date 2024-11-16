# Crop Recommendation System

This repository contains a machine learning project aimed at building and evaluating models for recommending suitable crops based on soil and climatic conditions. By leveraging features like soil nutrients (Nitrogen, Phosphorus, Potassium), temperature, humidity, pH, and rainfall, the project applies four different classifiers to identify the best-performing model for crop recommendation.

## Dataset
The dataset used in this project is sourced from Kaggle: [Crop Recommendation Dataset](https://www.kaggle.com/datasets/siddharthss/crop-recommendation-dataset). It provides labeled data for various crops with environmental features.

## Features
The dataset includes the following features:
- **N**: Nitrogen content in soil
- **P**: Phosphorus content in soil
- **K**: Potassium content in soil
- **temperature**: Temperature (°C)
- **humidity**: Relative humidity (%)
- **ph**: pH value of the soil
- **rainfall**: Rainfall (mm)
- **label**: Recommended crop type (target variable)

## Project Workflow
1. **Data Preprocessing**
   - Missing value analysis (none found in this dataset).
   - Label encoding for the target variable.
   - Standardization of features to ensure uniform scaling.

2. **Model Selection**
   - The following classifiers were evaluated:
     - Logistic Regression
     - K-Nearest Neighbors (KNN)
     - Random Forest
     - Gradient Boosting

3. **Model Evaluation**
   - Used 5-fold cross-validation to ensure robust performance metrics.
   - Metrics evaluated:
     - Accuracy
     - Precision (weighted)
     - Recall (weighted)
     - F1 Score (weighted)

## Results
The results of the 5-fold cross-validation for each model are as follows:

| Model                 | Accuracy | Precision | Recall | F1 Score |
|-----------------------|----------|-----------|--------|----------|
| Logistic Regression   | 97.14%   | 97.34%    | 97.14% | 97.12%   |
| K-Nearest Neighbors   | 97.14%   | 97.44%    | 97.14% | 97.12%   |
| Random Forest         | **99.32%** | **99.38%** | **99.32%** | **99.32%** |
| Gradient Boosting     | 99.14%   | 99.20%    | 99.14% | 99.14%   |

**Random Forest Classifier** outperformed the other models, making it the best choice for crop recommendation based on the given dataset.

## Conclusion
This project demonstrates how machine learning can optimize agricultural practices by recommending the most suitable crops for a given environment. Enhancing the data collection process with IoT technology can further improve the accuracy and usability of such systems. 

Data for features like nutrient levels, pH, temperature, humidity, and rainfall can be gathered in the following ways:

### Nutrient Levels and pH
1. **Manual Collection**: Soil samples can be collected manually and analyzed in laboratories for nutrient levels and pH.  
2. **Aerial Vehicles**: Quadcopter drones equipped with sensors can remotely collect soil samples and analyze them in real time.  
3. **IoT Sensors**: IoT-enabled devices like Teralytic Sensors can be deployed directly in the field to provide real-time analyses of soil mineral levels and pH.  

### Temperature, Humidity, and Rainfall
1. **Weather Stations**: Installing weather stations in the field to measure environmental parameters such as temperature, humidity, and rainfall.  
2. **Web-Based Data**: Accessing reliable weather data from web-based APIs for real-time and historical weather conditions.

### Enhancing Agricultural Practices
By leveraging such a network of sensors and data collection methods, this system can not only recommend the best possible crops but also provide tailored farming practices to enhance crop yield, particularly in agricultural regions like Pakistan. These advancements can lead to smarter resource utilization and improved agricultural productivity.
