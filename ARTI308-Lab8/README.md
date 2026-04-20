# 📘 K-Nearest Neighbors (KNN) Assignment

This project demonstrates how to use the K-Nearest Neighbors (KNN) algorithm with scikit-learn to classify data from the `KNN_Project_Data.csv` dataset.

## 📂 Dataset
The dataset contains several numerical features and a target column called **`TARGET CLASS`**, which the model predicts.

## ⚙️ Workflow
- Load and explore the dataset using pandas
- Scale features with `StandardScaler`
- Split data into training and testing sets
- Train a KNN model using `KNeighborsClassifier`
- Evaluate performance with a confusion matrix and classification report
- Test multiple K values to find the optimal one using error rate

## 📊 Results
Model performance improves after selecting an appropriate K value, reducing the error rate and increasing accuracy.

## 🛠️ Libraries Used
- pandas
- numpy
- matplotlib
- scikit-learn
