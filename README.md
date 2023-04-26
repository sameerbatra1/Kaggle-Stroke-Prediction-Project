# Kaggle-Stroke-Prediction-Project

## Introduction
According to the World Health Organization (WHO) stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths.
This dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases, and smoking status. Each row in the data provides relavant information about the patient.

Link to the dataset:
https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset

## Attribute Information
1) id: unique identifier
2) gender: "Male", "Female" or "Other"
3) age: age of the patient
4) hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
5) heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
6) ever_married: "No" or "Yes"
7) work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8) Residence_type: "Rural" or "Urban"
9) avg_glucose_level: average glucose level in blood
10) bmi: body mass index
11) smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
12) stroke: 1 if the patient had a stroke or 0 if not
* Note: "Unknown" in smoking_status means that the information is unavailable for this patient

## About My Work
* I used Pandas, NumPy, Seaborn, and Matplotlib to manipulate and analyze this dataset. 

* While manipulating the data, I found that there was only one row with the gender 'Other'. Considering this an outlier, I deleted the entire row. Now, my dataset only contains two genders: Male and Female.

* To avoid overfitting, I used the cross-validation feature of Scikit-Learn. 
 
* This dataset had several object data types which I converted to categorical data types. Then, I used one-hot encoding and a column transformer to convert the data into numeric form.

* I trained models using multiple algorithms and identified the best one. The algorithms I used were Random Forest Classifier, Support Vector Classifier (SVC), K-Nearest Neighbors Classifier (KNeighborsClassifier), and Linear Regression.

* I also applied feature importance to the Random Forest Classifier, which showed that BMI had the greatest contribution to the model, followed by work type, ever married, and smoking status.
