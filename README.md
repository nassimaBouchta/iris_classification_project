
# 🌸 Iris Species Classification

## 📖 Overview
This project is a classic Machine Learning classification task. The goal is to predict the species of an Iris flower (*Setosa*, *Versicolor*, or *Virginica*) based on the physical measurements of its sepals and petals. 

This project demonstrates the end-to-end Data Science pipeline: from handling raw data and splitting it, to training machine learning models and evaluating their performance.

## 📊 The Dataset
The famous **Iris Dataset** is used for this project. It contains:
* **150 instances** (rows) of Iris flowers.
* **4 Features** (measurements in cm): Sepal Length, Sepal Width, Petal Length, Petal Width.
* **1 Target Variable**: The Species of the flower (3 classes).

## 🛠️ Technologies Used
* **Python 3**
* **Pandas:** For data manipulation and cleaning.
* **NumPy:** For numerical operations.
* **Scikit-Learn (sklearn):** For machine learning algorithms, data splitting, and evaluation metrics.
* **Matplotlib / Seaborn:** For data visualization.

## 🚀 Methodology & Workflow

### 1. Data Loading & Inspection
Loaded the dataset using Pandas. Inspected the data using `.info()` and `.isnull()` to ensure there were no missing values and to verify data types. Dropped the unnecessary `Id` column to prevent the model from learning useless patterns.

### 2. Data Preprocessing
Separated the features (`X`) from the target variable (`y`). 
Used `train_test_split` to divide the data into:
* **Training Set (80%):** Used to teach the model.
* **Testing Set (20%):** Used as a "final exam" to evaluate real-world performance.
*(Note: `random_state=42` was used to ensure reproducibility).*

### 3. Model Training
Two classification algorithms were trained and compared:
1. **Decision Tree Classifier:** A highly interpretable model that creates a flowchart of yes/no questions.
2. **Random Forest Classifier:** An ensemble method that uses an "army" of 100 decision trees and takes a majority vote, reducing the risk of overfitting.

### 4. Model Evaluation
Evaluated the models on the unseen Test Set using:
* **Accuracy Score:** Overall percentage of correct predictions.
* **Classification Report:** Precision, Recall, and F1-Score for each individual species.

## 🏆 Results
Both the Decision Tree and the Random Forest models achieved a **100% accuracy rate** on the test set. 

*Note: While 100% accuracy is rare in real-world, messy datasets, the Iris dataset is highly separable, making it an excellent benchmark for understanding classification algorithms.*

## 💡 Key Learnings
* Understood the critical importance of **Train/Test splitting** to prevent overfitting.
* Learned how **Decision Trees** use mathematical purity (Gini impurity) to split data.
* Explored **Ensemble Learning** (Random Forest) to create more robust models.
* Learned how to serialize (pickle) a trained model to deploy it in a real-world application.
