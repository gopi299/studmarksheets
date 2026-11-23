<html> 
<head>
Marksheets</head>
<body>

<h1># Student Marksheet Analysis & Age Prediction</h1>
<br>
<br>


<p>A machine learning and exploratory data analysis (EDA) project built with Python that processes student marksheet data, visualizes feature correlations, and trains a Linear Regression model to predict student age.<p>

<h2>
Project Overview 
   
**1. Data Collection**
Collected student information from Marksheets.csv.

Dataset contains 100 student records and 9 columns.

Includes demographic details and marks in four subjects.

2. Data Exploration
Used Pandas to understand the dataset structure.

Checked column names, data types, and dimensions.

Generated statistical summaries using describe().

3. Data Cleaning
Verified missing values using isnull().sum().

Checked the dataset for data completeness.

Prepared the dataset for further analysis.

4. Data Preprocessing
Applied Label Encoding to convert categorical values into numerical format.

Removed unnecessary columns such as Name and Section.

Prepared numerical data for analysis and model building.

5. Exploratory Data Analysis (EDA)
Analyzed student demographic details and academic performance.

Studied relationships between subject marks and student age.

Used correlation analysis to understand feature relationships.

6. Data Visualization
Created a correlation heatmap using Seaborn.

Used Matplotlib for graphical representation.

Identified positive and negative relationships between numerical variables.

7. Model Building
Selected Linear Regression as the machine learning algorithm.

Identified Age as the target variable.

Selected relevant student details and subject marks as input features.

8. Model Training and Testing
Divided the dataset into 80% training data and 20% testing data.

Trained the Linear Regression model using Scikit-Learn.

Prepared the model for predicting student age.

9. Model Serialization
Used Joblib to save the trained model.

Exported the model as evebatch.pkl.

Enabled future model loading without retraining.

10. Future Improvements
Remove Age from the input features to avoid data leakage.

Improve prediction accuracy through proper feature selection.

Evaluate model performance using MAE, MSE, RMSE, and R² score.

Explore additional machine learning algorithms.

Develop a user-friendly interface for making predictions.

🎯 Conclusion
This project successfully demonstrates the implementation of a basic Machine Learning workflow using Python. It provides practical experience in handling student datasets, performing data preprocessing, conducting exploratory data analysis, visualizing correlations, and developing a Linear Regression model.

By utilizing libraries such as Pandas, NumPy, Matplotlib, Seaborn, and Scikit-Learn, the project helps understand how real-world data can be analyzed and used for machine learning applications.

The trained model is saved as evebatch.pkl using Joblib, allowing it to be reused for future predictions without repeating the training process.

Overall, this project provides a strong foundation in Data Analysis and Machine Learning, while offering opportunities for future improvements in model accuracy, reliability, and deployment.

Project
Summary
 The project covers the complete machine learning pipeline, from data collection to model serialization, with an important scope for improvement by eliminating target-variable leakage before final model evaluation.



</body>
</html>

