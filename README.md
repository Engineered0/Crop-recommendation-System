# Crop-recommendation-System


## Project Overview

**Objective:** Develop a machine learning model to recommend suitable crops based on various soil and environmental factors.

**Data Source:** The dataset used includes features such as Nitrogen (N), Phosphorus (P), Potassium (K), temperature, humidity, pH, and rainfall.

## Data Exploration and Preprocessing

1. **Data Loading:**
   - Data is loaded into a pandas DataFrame from 'Crop_recommendation.csv'.

2. **Data Cleaning:**
   - Renaming columns for clarity.
   - Checking and handling missing values.

3. **Exploratory Data Analysis (EDA):**
   - Statistical summary of the data.
   - Visualization of relationships between different features and crop types.

4. **Feature Selection:**
   - All given features are used for model training.

## Model Development

1. **Data Splitting:**
   - The dataset is split into training and test sets with a test size of 25%.

2. **Model Training:**
   - A Random Forest Classifier is used within a MultiOutputClassifier framework for multi-class classification.
   - Hyperparameters are optimized using GridSearchCV.

3. **Model Evaluation:**
   - The model is evaluated based on accuracy.
   - Cross-validation is used to assess the model's stability.

## Results

- The Random Forest Classifier achieved an accuracy of 98% on the test dataset.
- Feature importance analysis revealed that [mention key features] are most predictive of crop type.

## Model Deployment

- The trained model is serialized and saved as 'crop_recommendation_model.pkl'.
- A function `recommend_crop` is created to make predictions using the model.

## Usage

To recommend a crop, input the values for Nitrogen, Phosphorus, Potassium, temperature, humidity, pH, and rainfall into the `recommend_crop` function.

Example:

recommended_crop = recommend_crop(90, 40, 40, 25, 80, 6.5, 100)
print(f"The recommended crop is: {recommended_crop}")

## Conclusion and Future Work

- The model demonstrates good potential in recommending crops based on environmental and soil conditions.
- Future work could include incorporating more data, trying different algorithms, or expanding the scope of the system.
