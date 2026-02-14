
# Problem Statement
The objective of this project is to implement and evaluate six different machine learning classification models to predict the quality of red wine based on its physicochemical properties. 
By comparing traditional classifiers with ensemble methods, we aim to identify the most robust model for distinguishing between "Good" and "Bad" wine quality, providing a data-driven approach to quality control in the winemaking process.

# Dataset Description
Dataset Name: Wine Quality Dataset (Red Wine)
Source: UCI Machine Learning Repository
Problem Type: Binary Classification (predicting if wine is "Good" or "Bad")
Instance Size: 1,599 samples 
Feature Size: 11 physicochemical input features + 1 target variable (Total 12).
Target Variable: The original 'quality' score (0-10) was transformed into a binary 
# classification task:
1 (Good): Quality score > 5.
0 (Bad): Quality score < 5.
# Input Features: 
Fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, and alcohol.
# Feature details
Fixed acidity: Non-volatile acids that do not evaporate readily.
Volatile acidity: The amount of acetic acid in wine.
Citric acid: Found in small quantities, adds 'freshness' to wine.
Residual sugar: Amount of sugar remaining after fermentation stops.
Chlorides: The amount of salt in the wine.
Free sulfur dioxide: Prevents microbial growth and oxidation of wine.
Total sulfur dioxide: Amount of free and bound forms of $SO_2$.
Density: The density of water based on the percent alcohol and sugar content.
pH: Describes how acidic or basic the wine is (0-14 scale).
Sulphates: A wine additive which can contribute to sulfur dioxide levels.
Alcohol: The percent alcohol content of the wine.
Target (Quality): Originally a score between 0 and 10, mapped to 0 (Bad: Quality < 5) and 1 (Good: Quality > 5).

# Models Used
The following comparison table summarizes the performance of all six implemented models across the mandatory evaluation metrics :

<img width="927" height="183" alt="image" src="https://github.com/user-attachments/assets/ca90ec9f-a1e5-4ae7-ae10-f53b5d1e9079" />


# Performance Observations
XGBoost emerged as the top-performing model, achieving the highest Accuracy (81.25%) and MCC (0.6203).
Ensemble methods (Random Forest and XGBoost) significantly outperformed standalone models, benefiting from reduced variance and improved generalization.
kNN showed the lowest performance, likely due to the high dimensionality of the 11 features without extensive feature scaling.

<img width="1395" height="180" alt="image" src="https://github.com/user-attachments/assets/47d5c963-8e23-43fc-8817-02e5c8943c22" />


**Logistic Regression,** "Showed moderate performance with a high Recall (0.86), suggesting it is good at identifying positive cases but has a lower MCC (0.37), indicating a weaker overall correlation than ensemble methods."

**Decision Tree,** "Significantly outperformed basic linear models in Accuracy (0.787) and MCC (0.51), effectively capturing non-linear patterns in the dataset."

**kNN,** "Tied for the lowest accuracy (0.711). It appears sensitive to the scale of features or noise in the data, resulting in the lowest MCC (0.316) among all models."

**Naive Bayes** Performed similarly to kNN in accuracy but maintained a better balance between Precision and Recall. It served as a solid baseline for probabilistic classification.

**Random Forest (Ensemble)** "Achieved the highest AUC (0.908), indicating excellent ability to distinguish between classes. It significantly reduced variance compared to the single Decision Tree."

**XGBoost (Ensemble)** Top Performer. Achieved the highest Accuracy (0.838) and MCC (0.628). The boosting approach provided the most robust predictions for this classification task.
