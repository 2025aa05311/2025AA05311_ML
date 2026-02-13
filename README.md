
# Problem Statement
The objective of this project is to develop a robust machine learning system to classify the quality of red wine based on its physicochemical properties. 
By comparing six different classification algorithms—ranging from linear models like Logistic Regression to complex ensembles like XGBoost—this project identifies the most effective model for quality prediction, which can help winemakers ensure consistency and quality control.

# Dataset Description
Dataset Name: Wine Quality Dataset (Red Wine)
Source: UCI Machine Learning Repository
Problem Type: Binary Classification (predicting if wine is "Good" or "Bad")
Instance Size: 1,599 samples 
Feature Size: 11 input features + 1 target variable (12 total columns)

# Feature details
Feature Details:Fixed acidity: Non-volatile acids that do not evaporate readily.Volatile acidity: The amount of acetic acid in wine.Citric acid: Found in small quantities, adds 'freshness' to wine.Residual sugar: Amount of sugar remaining after fermentation stops.Chlorides: The amount of salt in the wine.Free sulfur dioxide: Prevents microbial growth and oxidation of wine.Total sulfur dioxide: Amount of free and bound forms of $SO_2$.Density: The density of water based on the percent alcohol and sugar content.pH: Describes how acidic or basic the wine is (0-14 scale).Sulphates: A wine additive which can contribute to sulfur dioxide levels.Alcohol: The percent alcohol content of the wine.Target (Quality): Originally a score between 0 and 10, mapped to 0 (Bad: Quality $\le$ 5) and 1 (Good: Quality > 5).


# Performance Observations
XGBoost emerged as the top-performing model, achieving the highest Accuracy (81.25%) and MCC (0.6203).
Ensemble methods (Random Forest and XGBoost) significantly outperformed standalone models, benefiting from reduced variance and improved generalization.
kNN showed the lowest performance, likely due to the high dimensionality of the 11 features without extensive feature scaling.
