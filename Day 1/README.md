# Student Performance Prediction & Analysis System

## Project Overview

This project focuses on predicting student academic outcomes using machine learning classification techniques.

The system uses student-related academic and behavioral features to predict whether a student is likely to pass or fail.

## Problem Statement

The objective of this project is to build a machine learning classification system that predicts the outcome of a student based on factors such as study hours, attendance, previous grades, assignment performance, midterm performance, absences, extracurricular participation, and parent education level.

## Dataset

### Dataset Source

The base dataset was obtained from Kaggle:

https://www.kaggle.com/datasets/souradippal/student-performance-prediction

The dataset used in this project was modified and extended from the source dataset before model development.

### Dataset Used

- Number of records: 10,000
- Number of columns: 9

### Input Features

- Study Hours per Week
- Attendance Rate
- Previous Grades
- Assignment Score
- Midterm Score
- Absences
- Participation in Extracurricular Activities
- Parent Education Level

### Target Variable

- Passed

The target variable represents whether the student passed or failed.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Machine Learning Workflow

1. Data loading
2. Data inspection
3. Data quality checking
4. Data cleaning
5. Missing-value checking
6. Categorical encoding
7. Exploratory Data Analysis
8. Train-test split
9. Feature scaling
10. Model training
11. Model evaluation
12. Model comparison
13. Final student prediction

## Data Preprocessing

The following preprocessing operations were performed:

- Checked for missing values
- Checked for duplicate records
- Checked numerical values for valid ranges
- Converted categorical features into numerical values
- Converted the target variable into binary form
- Split the data into training and testing sets
- Applied StandardScaler to the features

The final dataset contained no missing values or duplicate records.

The categorical features were encoded using binary encoding and one-hot encoding.

The dataset was divided into:

- 80% training data
- 20% testing data

## Exploratory Data Analysis

The project performs exploratory analysis using:

- Target variable distribution
- Feature distributions
- Histograms
- Box plots
- Correlation heatmap
- Relationships between features and student outcomes

### Key Observations

- The target variable is balanced, with 5,000 students marked as Pass and 5,000 marked as Fail.
- Study hours are mostly concentrated around the middle range, with fewer students having very low or very high study hours.
- Attendance rates are mostly concentrated between approximately 70% and 90%.
- Previous grades, assignment scores, and midterm scores show a wide range of student performance.
- Most students have a relatively low number of absences, while a smaller number have high absences.
- The box plots show differences in the distributions of academic features between passing and failing students.
- The numerical features do not show strong correlations with each other, indicating that the features provide relatively different information.

## Machine Learning Models

Two classification algorithms were developed and evaluated.

### Logistic Regression

Logistic Regression was used as one of the classification models for predicting the binary student outcome.

It provides a simple and interpretable approach for binary classification.

### K-Nearest Neighbors (KNN)

KNN was used as the second classification model.

Feature scaling was applied before using KNN because the algorithm is based on distances between data points.

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 62.90% | 63.28% | 63.91% | 63.59% |
| KNN | 60.15% | 60.93% | 59.66% | 60.29% |

### Confusion Matrix

#### Logistic Regression

```text
[[610, 376],
 [366, 648]]
```

#### KNN

```text
[[598, 388],
 [409, 605]]
```

## Model Comparison

Based on the evaluation results, Logistic Regression achieved higher accuracy, precision, recall, and F1 score than KNN on the test dataset.

Therefore, Logistic Regression was selected as the final model for the student prediction system.

Logistic Regression achieved an accuracy of 62.90%, while KNN achieved an accuracy of 60.15%.

## Student Prediction

The final prediction mechanism accepts the following information for a new student:

- Study hours per week
- Attendance rate
- Previous grades
- Assignment score
- Midterm score
- Absences
- Extracurricular activity participation
- Parent education level

The trained Logistic Regression model then predicts either:

- Pass
- Fail

### Sample Prediction

Example input:

- Study Hours: 20
- Attendance: 85
- Previous Grades: 75
- Assignment Score: 80
- Midterm Score: 78
- Absences: 3
- Extracurricular Activities: Yes
- Parent Education: Bachelor

Output:

```text
Prediction: Pass
```

## Screenshots

Important screenshots from the project are included in the `screenshots` folder.

Suggested screenshots:

- Dataset and preprocessing
- Exploratory Data Analysis
- Model evaluation
- Final prediction

## Limitations

- The prediction is based only on the features available in the dataset.
- Student performance can also be affected by factors such as motivation, learning environment, teaching quality, and personal circumstances, which are not included in the dataset.
- The model does not guarantee the actual academic outcome of a student.
- The current models provide moderate predictive performance, with Logistic Regression achieving 62.90% accuracy.
- The dataset is based on a limited set of student-related features and may not represent all student populations.
- Model performance may change when applied to a different dataset or real-world student population.

## Future Improvements

The system can be improved in the future by:

- Adding more relevant student performance features.
- Using larger and more diverse real-world datasets.
- Testing additional classification algorithms.
- Performing hyperparameter tuning.
- Applying feature selection techniques.
- Comparing different preprocessing approaches.
- Using cross-validation for more reliable model evaluation.
- Developing a simple web interface for entering student information.
- Deploying the prediction system as a web application.
- Continuously evaluating the model using new student data.

## Project Structure

```text
student-performance-prediction/
│
├── datasets/
│   └── student_performance_data.csv
│
├── notebook/
│   └── student_performance_prediction.ipynb
│
├── screenshots/
│   ├── dataset.png
│   ├── eda.png
│   ├── model_results.png
│   └── prediction.png
│
├── README.md
├── requirements.txt
└── .gitignore
```

## Requirements

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
```

## How to Run

1. Clone the repository.
2. Install the required Python libraries.
3. Place the dataset in the `datasets` folder.
4. Open the Jupyter Notebook.
5. Run the notebook cells sequentially.
6. Enter student information when prompted for the final prediction.

## Video Demonstration

_Add your Google Drive or YouTube Unlisted video link here._

The video demonstrates:

- Dataset
- Problem statement
- Data preprocessing
- Exploratory Data Analysis
- Feature selection
- Model development
- Model evaluation
- Model comparison
- Final prediction

## Project Status

- Dataset preparation
- Data preprocessing
- Exploratory Data Analysis
- Logistic Regression model
- KNN model
- Model evaluation
- Model comparison
- Student prediction mechanism

## Conclusion

This project demonstrates a complete machine learning classification workflow for predicting student academic outcomes.

The dataset was explored and prepared by checking data quality, encoding categorical variables, splitting the dataset into training and testing sets, and applying feature scaling.

Two classification models, Logistic Regression and K-Nearest Neighbors, were developed and evaluated using accuracy, precision, recall, F1 score, and confusion matrices.

Logistic Regression achieved the best overall performance with an accuracy of 62.90% and was therefore selected as the final model.

The project demonstrates how machine learning can be applied to student performance analysis and can serve as a foundation for developing a more advanced student performance prediction system.
