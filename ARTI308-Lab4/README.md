# 📊 Lab 4: Data Preprocessing and PCA Analysis

## 📌 Overview
This lab focuses on data preprocessing techniques and dimensionality reduction using Principal Component Analysis (PCA). The objective was to identify data quality issues, handle missing values, detect and manage outliers, normalize numerical features, and interpret PCA results.

---

## 🗂 Dataset
The dataset contains car-related information with the following features:

- Car ID  
- Brand  
- Year  
- Engine Size  
- Fuel Type  
- Transmission  
- Mileage  
- Condition  
- Price  
- Model  

---

## ✅ Task 1: Identify Data Quality Issues
- Inspected dataset using `.info()` and `.describe()`
- Checked for missing values
- Verified data types

**Finding:** Missing values were present in numerical columns.

---

## ✅ Task 2: Handle Missing Values
- Applied a missing value strategy (dropping or imputing missing values)
- Ensured no NaN values remained before scaling and PCA

**Reason:** PCA and scaling methods do not support missing values.

---

## ✅ Task 3: Detect and Handle Outliers (IQR Method)

Used the Interquartile Range (IQR) method:

- IQR = Q3 − Q1  
- Lower Bound = Q1 − 1.5 × IQR  
- Upper Bound = Q3 + 1.5 × IQR  

Values outside this range were considered outliers.

**Result:** No statistical outliers were detected using the 1.5×IQR rule.

---

## ✅ Task 4: Feature Normalization

Two scaling techniques were applied:

### 🔹 Min-Max Scaling
- Scales values between 0 and 1

### 🔹 Z-Score Standardization
- Mean = 0  
- Standard deviation = 1  

Scaling ensures that no feature dominates due to larger magnitude.

---

## ✅ Task 5: Principal Component Analysis (PCA)

- Applied PCA with `n_components = 2`
- Used standardized numerical features (Price and Mileage)
- Evaluated explained variance ratio

**Interpretation:**  
The first principal component explains the majority of the variance, meaning most of the dataset’s variability can be summarized along a single direction.

---

## 🛠 Tools Used
- Python  
- Pandas  
- NumPy  
- Scikit-learn  

---

## 📈 Conclusion
This lab demonstrated a complete preprocessing workflow:

1. Data inspection  
2. Missing value handling  
3. Outlier detection  
4. Feature scaling  
5. Dimensionality reduction using PCA  

The dataset was successfully cleaned, normalized, and analyzed.