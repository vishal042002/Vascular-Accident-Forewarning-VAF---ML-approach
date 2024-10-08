Stroke Prediction Project
This project focuses on predicting the likelihood of a stroke based on various health and lifestyle factors. The dataset used for this project is sourced from Kaggle and explores the impact of attributes such as age, gender, BMI, glucose levels, and pre-existing medical conditions on stroke occurrence.
Project Motivation
Strokes are a serious health concern, and early prediction plays a crucial role in timely intervention and potentially mitigating its impact. By building a predictive model, this project aims to assist healthcare professionals in identifying individuals at higher risk of stroke, enabling them to provide personalized care and guidance.
Dataset
The dataset used is "healthcare-dataset-stroke-data.csv" from Kaggle. It contains information about patients, including:

Demographic information: Gender, Age, Residence Type (Urban/Rural)

Medical History: Hypertension, Heart Disease

Lifestyle: Smoking Status

Physiological Indicators: Average Glucose Level, BMI

Target Variable: Stroke (Binary: 0 - No Stroke, 1- Stroke)
Methodology

Data Loading and Preprocessing: The dataset is loaded using Pandas. The 'id' column, being irrelevant to stroke prediction, is removed.

Exploratory Data Analysis (EDA): EDA is performed to gain insights into the dataset. This includes analyzing each feature individually and visualizing relationships with the target variable using histograms, box plots, countplots, and pie charts.

Data Cleaning and Transformation: Missing values in the BMI column are handled by imputing them with the median. Categorical features are converted into numerical format using dummy variable creation (one-hot encoding). The data is standardized using StandardScaler to bring all numerical attributes to a similar scale.

Addressing Class Imbalance: The dataset exhibits a class imbalance with a significantly lower proportion of stroke cases. To handle this, random oversampling is implemented using the imblearn library, ensuring balanced representation for both classes during model training.

Model Building: Various classification models are trained and evaluated. The project experiments with:

Decision Tree Classifier

K-Nearest Neighbors (KNN)

XGBoost Classifier

Random Forest Classifier

Logistic Regression

Model Evaluation: The performance of each model is assessed using metrics such as Accuracy, ROC AUC Score, Precision, Recall, and F1-score.

Hyperparameter Tuning and Cross-Validation: The models are further optimized using techniques like RandomizedSearchCV and cross-validation to enhance their generalization capabilities and achieve better performance.

Model Deployment: The final chosen model (Random Forest) is saved using pickle.
Results
The XGBoost and Random Forest models demonstrated the highest accuracy of 97.63% and 99.48% respectively in predicting strokes. The project provides insights into the factors influencing stroke prediction.
Future Work
This project has room for expansion:

Further hyperparameter tuning can potentially enhance model performance.

Exploring more complex ensemble techniques might yield more robust predictions.

Incoporating a wider range of features relevant to stroke prediction.
