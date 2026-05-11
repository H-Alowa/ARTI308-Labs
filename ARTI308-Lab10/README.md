# Support Vector Machine Iris Classification

## Project Overview

This project is a machine learning assignment that uses a **Support Vector Machine (SVM)** classifier to predict iris flower species from the classic Iris dataset. The notebook walks through loading the data, visualizing the feature relationships, training an SVM model, evaluating its performance, and tuning model parameters with `GridSearchCV`.

The dataset contains 150 iris flower samples from three species:

- Iris setosa
- Iris versicolor
- Iris virginica

Each sample includes four measured features:

- Sepal length
- Sepal width
- Petal length
- Petal width

## Files

- `02-SVM Assignment.ipynb` — main Jupyter Notebook containing the full assignment workflow.
- `README_svm_assignment.md` — this README file.

## Tools and Libraries Used

The notebook uses the following Python libraries:

- `pandas` for data handling
- `numpy` for numerical operations
- `matplotlib` and `seaborn` for data visualization
- `scikit-learn` for model training, evaluation, train/test splitting, SVM, and grid search

## Workflow

1. **Load the Iris dataset** using Seaborn.
2. **Explore the data** with visualizations, including:
   - Pairplot by species
   - KDE plot for setosa sepal length and sepal width
3. **Split the dataset** into training and testing sets using a 70/30 split.
4. **Train an SVM classifier** using `SVC()` from scikit-learn.
5. **Evaluate the model** with:
   - Classification report
   - Confusion matrix
6. **Tune hyperparameters** using `GridSearchCV` with different values of `C` and `gamma`.
7. **Compare performance** before and after parameter tuning.

## Model Results

The initial SVM model performed very well on the test set, achieving about **98% accuracy**.

The confusion matrix for the original model was:

```text
[[13  0  0]
 [ 0 19  1]
 [ 0  0 12]]
```

After using GridSearchCV, the best parameters were:

```python
{'C': 1, 'gamma': 0.1}
```

The tuned model achieved the same overall accuracy of about **98%**, so the grid search did not significantly improve the model. This is expected because the Iris dataset is small and already highly separable, especially for the setosa class.
