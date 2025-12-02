Hybrid Expert System for Food Nutrition Classification

This mini-project focuses on building a Hybrid Expert System that uses both rule-based logic and a machine learning model to classify food items as healthy or unhealthy based on their nutritional values. The main objective was to understand how expert systems can work together with machine learning to create a smarter and more explainable decision-making system.

Project Overview

The system uses two different rule mechanisms that serve different purposes.

1. Rule-Based System for Label Creation (Training Stage)

The dataset did not contain a “healthy” or “unhealthy” column.
To train the machine learning model, it was necessary to create labels first.
A simple rule was used to assign healthy (1) or unhealthy (0) based on calorie, fat, and carbohydrate thresholds.

These label rules were used only at the training stage to generate the target column.
They are not used during the final prediction stage.

This step is known as label engineering.

2. Knowledge-Based Expert Rules (Prediction Stage)

A separate rule set was used during prediction.
These rules classify very clear cases directly.
If the rule does not confidently decide, the system forwards the decision to the machine learning model.

This forms the hybrid decision system, where the expert rules handle simple cases and the machine learning model handles more complex ones.

Hybrid Decision Flow

The prediction process follows these steps:

1. The system first checks the expert rules.
2. If the rule gives a clear decision, that output is returned.
3. If the rule cannot decide, the RandomForest model makes the prediction.
4. The final result is a combination of both rule logic and machine learning.

Dataset

The dataset used was the Food Nutrition Dataset from Kaggle.
It includes nutritional values such as calories, protein, carbs, fat, iron, and vitamin C.
A new column called “healthy” was created using the label rules defined earlier.

Technologies Used

Python
Pandas
NumPy
Scikit-learn
Google Colab

Main Features Implemented

Data cleaning and preprocessing
Rule-based label creation
Expert system rules for prediction
RandomForest model training
Model evaluation using classification report and confusion matrix
Feature importance analysis
Final hybrid decision-making system

How to Run the Project

Open the notebook in Google Colab.
Upload the dataset file.
Run all cells step by step.
Use the final cell to test the hybrid system with any food item.

Example Output (Hybrid System)

Rule decision: Use ML
Machine Learning prediction: Unhealthy
Hybrid prediction: Unhealthy

Model Insights:

The RandomForest model found calories, carbs, and fat to be the most important features for determining whether a food item is healthy.

Future Improvements:

Include additional nutrition features such as fiber and sodium.
Use more advanced machine learning models such as XGBoost.
Create a simple user interface for prediction.
Add image-based nutrition estimation.
Deploy the model as a web application.

Author

Gurudeep Ravilla
GitHub: [https://github.com/GurudeepRavilla](https://github.com/GurudeepRavilla)

