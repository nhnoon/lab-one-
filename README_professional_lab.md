
# Data Quality Assessment & Preprocessing Lab
**Course:** ARTI308 – Machine Learning  
**Dataset:** Heart Disease Dataset  

---

# 1. Introduction
Data preprocessing is a critical step in any machine learning pipeline. Raw data often contains issues such as missing values, outliers, inconsistent scales, and redundant features. If these issues are not handled properly, they can significantly affect the performance of machine learning models.

In this lab, we perform a complete **data quality assessment and preprocessing workflow** using the **Heart Disease dataset**. The goal is to clean, analyze, and transform the dataset so it becomes suitable for machine learning algorithms.

---

# 2. Objectives
The main objectives of this lab are:

- Assess the quality of the dataset
- Detect and handle missing values
- Calculate descriptive statistics (Mean, Median, Percentiles)
- Detect outliers using the **Interquartile Range (IQR)**
- Normalize numerical features using **Min-Max scaling**
- Standardize data using **Z-score normalization**
- Analyze relationships between variables using **Correlation Matrix**
- Reduce dimensionality using **Principal Component Analysis (PCA)**

---

# 3. Dataset Description
The **Heart Disease dataset** contains medical measurements used to predict the presence of heart disease.

Each row represents a **patient record**, and each column represents a **clinical measurement**.

### Key Features

| Feature | Description |
|-------|-------------|
| age | Age of the patient |
| chol | Cholesterol level |
| trestbps | Resting blood pressure |
| thalach | Maximum heart rate achieved |
| oldpeak | ST depression induced by exercise |
| target | Indicates presence of heart disease |

The dataset contains multiple numerical features that make it suitable for statistical analysis and preprocessing.

---

# 4. Methodology

## Step 1 – Import Libraries
The following Python libraries are used:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

These libraries are essential for data manipulation, visualization, and preprocessing.

---

## Step 2 – Load Dataset
The dataset is loaded using **pandas** and inspected to verify:

- dataset structure
- number of rows and columns
- data types

This helps understand the dataset before performing preprocessing operations.

---

## Step 3 – Data Quality Assessment
The dataset is analyzed to identify potential issues including:

- missing values
- inconsistent data types
- abnormal distributions

Statistical summaries are generated to understand the spread and central tendencies of numerical features.

---

# 5. Statistical Analysis

## Mean and Median
The **mean** represents the average value of the data, while the **median** represents the middle value after sorting the data.

Visualizing both statistics helps identify skewed distributions or potential outliers.

### Visualization
A histogram is used to visualize the distribution of the **cholesterol feature** with mean and median markers.

---

## Percentiles
Percentiles divide the dataset into ordered segments.

Key percentiles used in this lab:

- 25th percentile (Q1)
- 50th percentile (Median)
- 75th percentile (Q3)

These values help measure the spread of the data.

---

# 6. Outlier Detection

Outliers are detected using the **Interquartile Range (IQR)** method.

### Formula

IQR = Q3 − Q1

### Outlier boundaries

Lower Bound = Q1 − 1.5 × IQR  
Upper Bound = Q3 + 1.5 × IQR

Values outside this range are considered **outliers**.

### Visualization
Boxplots are used to visualize the presence of outliers in numerical features.

---

# 7. Normalization Techniques

Different machine learning algorithms require features to be on a similar scale.

Two normalization techniques are applied:

### Min-Max Scaling

Transforms data to the range:

0 ≤ X ≤ 1

Formula:

X_scaled = (X − X_min) / (X_max − X_min)

---

### Z-score Standardization

Transforms the data so that:

Mean = 0  
Standard deviation = 1

Formula:

Z = (X − μ) / σ

This method is commonly used before applying PCA.

---

# 8. Correlation Analysis

A **correlation matrix** is generated to measure relationships between numerical features.

The correlation heatmap helps identify:

- strongly related features
- redundant information
- potential dimensionality reduction opportunities

---

# 9. Principal Component Analysis (PCA)

PCA is a dimensionality reduction technique that transforms the dataset into a new coordinate system.

The first principal component captures the **largest variance**, while the second captures the **second largest variance**.

In this lab:

- PCA reduces the dataset to **two components**
- A scatter plot visualizes the transformed data

---

# 10. Results

Running the notebook generates the following outputs:

- Mean and Median calculations
- Histogram visualizations
- Percentile calculations
- IQR and outlier detection
- Boxplots for numerical features
- Min-Max normalized dataset
- Z-score standardized dataset
- Correlation heatmap
- PCA visualization

These outputs confirm that the dataset has been successfully analyzed and preprocessed.

---

# 11. How to Run the Lab

Place the following files in the same folder:

heart_preprocessing_lab.ipynb  
heart.csv  
README.md

Then:

1. Open the notebook in **VS Code** or **Jupyter Notebook**
2. Run all cells
3. Verify that all plots and outputs are generated

---

# 12. Conclusion

This lab demonstrates the importance of **data preprocessing in machine learning**.

The main preprocessing tasks performed include:

- data quality assessment
- statistical analysis
- outlier detection
- normalization
- correlation analysis
- dimensionality reduction using PCA

These steps ensure that the dataset is clean, well-structured, and suitable for building accurate machine learning models.

---
