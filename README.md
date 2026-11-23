<html> 
<head>
Marksheets</head>
<body>

<h1># Student Marksheet Analysis & Age Prediction</h1>
<br>
<br>


<p>A machine learning and exploratory data analysis (EDA) project built with Python that processes student marksheet data, visualizes feature correlations, and trains a Linear Regression model to predict student age.<p>

<h2>## 📋 Project Overview</h2>
<p>This project analyzes a dataset of 100 student records (`Marksheets.csv`) containing demographic details and academic scores across four subjects. The workflow covers data loading, summary statistics, missing value verification, categorical encoding, correlation visualization, model training, and model serialization.
<
<2><u>## 📊 Dataset Description</u></h2>
<p>
The dataset (`Marksheets.csv`) consists of **100 rows and 9 columns**:
* **`id`**: Student identification number
* **`Name`**: Student's name
* **`Gender`**: Student's gender (`Male` / `Female`)
* **`Age`**: Age of the student (Target variable, ranging from 13 to 15)
* **`Section`**: Assigned class section (`A`, `B`, or `C`)
* **`Science`**, **`English`**, **`History`**, **`Maths`**: Subject marks (ranging from 1 to 100)

<2>## 🛠️ Technologies Used<2>
<p>* **Python**
* **NumPy & Pandas**: Data manipulation, cleaning, and statistical analysis
* **Matplotlib & Seaborn**: Data visualization and correlation heatmap generation
* **Scikit-Learn**: Label encoding, train-test splitting, and Linear Regression modeling
* **Joblib**: Saving and loading the trained model (`evebatch.pkl`)
</p>

<h2>## ⚙️ Workflow & Key Steps<h2>
<p>
1. **Data Exploration & Cleaning**: Checked data types (`info()`), statistical summaries (`describe()`), and verified zero missing values across all columns (`isnull().sum()`).
2. **Preprocessing**: Encoded the `Gender` column using `LabelEncoder` and dropped non-numeric columns (`Name`, `Section`, `Gender`) for correlation and modeling.
3. **Exploratory Data Analysis (EDA)**: Generated a Seaborn correlation heatmap to inspect relationships between subject scores and age.
4. **Model Training**: Split the dataset into training (80%) and testing (20%) sets (`test_size=0.2`) and fitted a `LinearRegression` model.
5. **Model Serialization**: Exported the trained model using `joblib` as `evebatch.pkl` for future inference.
</p>
<h3>## 🚀 How to Run</h3>
1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd your-repo-name
   ```

2. **Install required dependencies:**
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn joblib
   ```

3. **Run the Jupyter Notebook:**
   Open the notebook file (`.ipynb`) in Jupyter Notebook or Anaconda, update the file path to `Marksheets.csv` if needed, and run all cells.

4. **Load the saved model for predictions:**
   ```python
   import joblib

   loaded_model = joblib.load('evebatch.pkl')
   # Input format: [[id, Age, Science, English, History, Maths]]
   prediction = loaded_model.predict([[82, 96, 89, 56, 50, 60]])
   print(prediction)
   ```

<h3><u> 💡 Note for Future Improvements</u></h3>
<p>
Currently, the target variable (`Age`) is included in the feature matrix `X` (`X = data.drop(["Name", "Section", "Gender"], axis=1)`), which causes data leakage (resulting in the model predicting the exact input age, e.g., `96.` when `96` is passed in the second position). Dropping `"Age"` from `X` before training will allow the model to genuinely predict age based solely on subject marks.
</p>
</body>
</html>
