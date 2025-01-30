# Machine Learning Algorithm Performance Analysis

## Introduction

In machine learning, the choice of algorithm is often viewed as the cornerstone of success. However, the performance of these algorithms is inherently tied to the data on which they are trained. This study aims to investigate how different machine learning algorithms perform on the same dataset, using a variety of methods and optimization techniques. The overarching goal is to understand not only how the models compare but also how much the dataset itself constrains their performance.

## Purpose of the Study

The primary objective of this study is to explore the capabilities and limitations of several popular machine learning algorithms, including:

- **Random Forest**  
- **XGBoost**  
- **Support Vector Machines (SVM)**  
- **Logistic Regression**  
- **Neural Networks (PyTorch implementation)**  
- **K-Nearest Neighbors (KNN)**  

By applying these models to a classification task, the study seeks to identify:

- Which algorithm performs best under default settings.  
- How optimization can impact performance.  
- The extent to which data quality and quantity influence results.  

## Methods Employed

To achieve these goals, the study utilizes the following methods:

### Baseline Model Evaluation

Each algorithm is trained and tested on the dataset without optimization to establish baseline metrics.

### Hyperparameter Optimization

Grid search and other tuning techniques are applied to each model to maximize performance.

### Performance Comparison

Metrics such as accuracy, precision, recall, and F1-score are used to evaluate and compare model performance.

### Analysis of Results

I have some insights about the relationship between model performance and data constraints.

## Environment and Dependencies

This study was conducted using **Google Colab with no GPU acceleration**.

### Required Python Version

To ensure compatibility with **Sweetviz**, use **Python 3.8 or higher**.

### Imports

```python
import pandas as pd
import sweetviz as sv
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.metrics import confusion_matrix, f1_score, classification_report, accuracy_score
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split, cross_val_score
from sklearn.neighbors import KNeighborsClassifier
```
How to Use This Repository

Clone the repository:

git clone https://github.com/christophergaughan/Algorithm_Competion_Diabetes_Dataset/tree/main

Here’s what should be included in `requirements.txt`:
| Package      | Minimum Version |
| ------------ | --------------- |
| pandas       | >=1.3.0         |
| sweetviz     | >=2.1.4         |
| matplotlib   | >=3.4.3         |
| seaborn      | >=0.11.2        |
| scikit-learn | >=0.24.2        |

If you want to generate an exact list of installed dependencies, run:
`pip freeze > requirements.txt`


License

This project is licensed under the MIT License.


# To see the `Sweetviz` data tables:
> sweetviz link = file:///Users/chrisgaughan/Desktop/Machine_Deep_learning/sweetviz_report.html

## What is Sweetviz?

Sweetviz is an open-source Python library that automates exploratory data analysis (EDA) and generates visually appealing and comprehensive HTML reports. It helps users quickly understand the structure and relationships within their data, making it an invaluable tool for data scientists, analysts, and machine learning practitioners.

### Key Features of Sweetviz

1. **Detailed Data Analysis**:
   - Provides a side-by-side comparison of datasets (e.g., training vs. testing data) or detailed analysis of a single dataset.
   - Includes summary statistics, feature correlations, distribution visualizations, and missing value analysis.

2. **Interactive HTML Reports**:
   - Generates reports that are easy to navigate, with interactive visualizations that provide insights at a glance.

3. **Target Analysis**:
   - Highlights relationships between features and the target variable, useful for classification or regression tasks.

4. **Customizable Comparisons**:
   - Allows comparisons between multiple datasets (e.g., train vs. test splits) to ensure consistency and identify potential data drift.

5. **Quick and Intuitive**:
   - Minimal setup and easy-to-use API make it ideal for rapid data analysis.

### Example Use Case

```
import sweetviz as sv

# Load your datasets (example with pandas)
import pandas as pd
train = pd.read_csv('train.csv')
test = pd.read_csv('test.csv')

# Generate and display a report
report = sv.compare([train, "Train Dataset"], [test, "Test Dataset"])
report.show_html("sweetviz_report.html")
```

