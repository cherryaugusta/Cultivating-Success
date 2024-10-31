# Cultivating Success: Leveraging Machine Learning to Optimize Crop Selection

This repository contains my solution and personal enhancements for the guided project **"Predictive Modeling for Agriculture"** from DataCamp on [DataCamp](https://www.datacamp.com/projects/1772).

## Project Introduction

Assessing soil health by measuring critical metrics such as nitrogen, phosphorus, potassium levels, and pH is essential for understanding soil conditions. However, this process can be both costly and time-intensive, often leading farmers to prioritize which metrics to measure based on financial constraints.

Farmers must make numerous decisions regarding which crops to plant each season, with the primary goal of optimizing crop yield. One significant factor influencing crop performance is soil condition, which can be evaluated by measuring essential elements such as nitrogen and potassium. Each crop has specific soil requirements that support its optimal growth and yield.

A farmer has sought assistance in applying machine learning to determine the best crop for a particular field. The dataset provided, titled `soil_measures.csv`, includes the following variables:

- "N": Nitrogen content ratio in the soil
- "P": Phosphorus content ratio in the soil
- "K": Potassium content ratio in the soil
- "pH": Soil pH value
- "crop": Categorical values representing different crops (target variable)

Each entry in the dataset reflects various soil measurements from a specific field, with the crop listed in the "crop" column being the ideal choice for that soil condition.

The goal of this project is to develop multi-class classification models to predict the crop type and identify the most critical feature contributing to predictive accuracy.

**Key Tools**: Python (Pandas, Scikit-learn)

## Analysis

An initial examination of the dataset reveals that the first several rows correspond exclusively to the crop "rice." Each row includes measurements for nitrogen (N), phosphorus (P), potassium (K), and soil pH. While these soil metrics vary, the consistent presence of "rice" in the `crop` column suggests that the conditions represented by these measurements are optimized for rice cultivation. This suggests that the dataset may focus on analyzing soil conditions particularly suited for growing rice.

The dataset consists of 2,200 entries with five columns: "N" (Nitrogen content), "P" (Phosphorus content), "K" (Potassium content), "ph" (pH value), and "crop" (crop type). All columns contain complete data with no missing values. The "N", "P", and "K" columns are stored as integers, while "ph" is stored as a float, and "crop" is represented as an object (categorical data). The dataset is well-structured, with consistent data types and fully populated fields, making it well-suited for further analysis.

The dataset contains 21 unique crop types, as shown below:
```
['rice', 'maize', 'chickpea', 'kidneybeans', 'pigeonpeas', 'mothbeans', 
'mungbean', 'blackgram', 'lentil', 'pomegranate', 'banana', 'mango', 
'grapes', 'watermelon', 'muskmelon', 'apple', 'orange', 'papaya', 
'coconut', 'cotton', 'jute', 'coffee']
```

This variety includes staple grains such as rice and maize, legumes like chickpea and mungbean, fruits such as pomegranate and mango, and other agricultural products like coffee and cotton. The diversity of crops suggests that the machine learning model will need to handle a broad classification task, accounting for different agricultural requirements and optimal soil conditions for each crop type.

### Best Predictive Feature: 

The analysis determined that potassium content ("K") is the most predictive feature, with a feature importance score of approximately 0.257. This indicates that the potassium level in the soil is the most significant factor in predicting the optimal crop for the soil conditions described in the dataset.

## Conclusion

The analysis of the dataset identifies potassium content ("K") as the most predictive feature in determining the optimal crop type for the soil conditions. With a feature importance score of approximately 0.257, potassium emerges as the most critical factor among the measured features for predicting crop suitability. These findings suggest that focusing on soil potassium levels may significantly enhance the accuracy of crop selection models.

## Acknowledgments
This project was developed as part of a DataCamp guided project. The original project can be found on [DataCamp](https://www.datacamp.com/projects/1772).
