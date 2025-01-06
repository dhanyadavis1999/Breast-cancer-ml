# A COMPARATIVE STUDY OF MACHINE LEARNING MODELS ON BREAST CANCER


This repository contains the work of a comparative study of machine learning models on breast cancer, part of my coursework at the University of Hertfordshire.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Dataset](#dataset)
4. [Exploratory Data Analysis](#exploratory-data-analysis)
5. [Data Preprocessing](#data-preprocessing)
6. [Model](#model)
7. [Model Assessment](#model-assessment)
8. [Conclusion](#conclusion)

---

## Project Overview

This is an individual project on breast cancer analysis, involving a comparative study between different machine learning models. The models used were Logistic Regression, Random Forest, and XGBoost, evaluated using various features and performance metrics.

---

## Objectives

1. To develop a machine learning model that can accurately classify breast tumors as benign or malignant based on diagnostic imaging data.  
2. To reduce the feature space while preserving important diagnostic data using dimensionality reduction techniques, such as PCA.  
3. To evaluate and compare the performance of multiple machine learning models (Random Forest, XGBoost, and Logistic Regression) using crucial measures such as F1-score, precision, recall, and AUC-ROC.  
4. To select the top-performing model for clinical usage, focusing on interpretability and generalization, based on the major accuracy metric.

---

## Dataset

The Breast Cancer Wisconsin (Original) dataset, used in this study, is available through the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic), and the data file is accessible [here](https://archive.ics.uci.edu/static/public/17/data.csv) under a Creative Commons (CC) license (Wolberg, W., 1990).  

- **Overview**: The dataset consists of 569 cases (357 benign and 212 malignant) with 30 numerical features derived from fine needle aspirations (FNA) of breast mass cell nuclei.  
- **Features**: Includes metrics such as area, perimeter, smoothness, symmetry, compactness, concavity, and texture.  
- **Challenge**: A slight class imbalance (benign cases outnumber malignant cases), reflecting real-world clinical scenarios where identifying malignant cases is crucial.

---

## Exploratory Data Analysis

Exploratory Data Analysis (EDA) involves a thorough analysis of the dataset to:
- Identify target labels and class imbalances.  
- Examine feature distributions and their relevance for classification tasks.  
- Use visualization tools such as bar plots, box plots, scatter plots, pair plots, and correlation heatmaps to identify key patterns, trends, and relationships.

Findings include:
- **Target Class Distribution**: Visualized the imbalance between benign and malignant cases.  
- **Feature Relationships**: Strong correlations between some features (e.g., radius1, perimeter1, area1) indicated redundancy, while unique contributions from others (e.g., smoothness1, fractal_dimension1) were noted.  

---

## Data Preprocessing

Key preprocessing steps included:

1. **Data Cleaning**: Verified no missing values using functions like `isnull()` and `sum()`.  
2. **Outlier Detection**: Removed outliers using the Z-score method to improve accuracy and precision.  
3. **Standardization**: Scaled features using standard scaling (zero mean and unit variance), essential for models like Logistic Regression.  
4. **Normalization**: Scaled features to a range of 0 to 1.  
5. **Dimensionality Reduction**: Applied Principal Component Analysis (PCA) after scaling to reduce dimensionality while preserving variance and eliminating multicollinearity.

---

## Model

Three machine learning models were created and refined:

1. **Logistic Regression**: Achieved a test accuracy of 93.75%, demonstrating strong generalization without overfitting.  
2. **Random Forest**: Achieved a test accuracy of 90.18%, with slightly reduced recall for malignant cases.  
3. **XGBoost**: Outperformed others with a test accuracy of 91.96%, effectively handling unbalanced data.

Performance metrics like F1-score, precision, recall, and AUC-ROC were used for evaluation, with AUC-ROC serving as the primary accuracy metric.

---

## Model Assessment

Evaluation metrics included:

- **Accuracy**: Proportion of correctly classified cases.
- **Precision**: Ratio of true positives to all predicted positives.
- **Recall**: Ratio of true positives to all actual positives.
- **F1-score**: Harmonic mean of precision and recall.
- **ROC-AUC**: Measured discriminative power across classification thresholds.

---

## Conclusion

This study developed an effective breast cancer prediction system using advanced machine learning methods, including Random Forest, XGBoost, and Logistic Regression. Thorough data preprocessing—such as feature selection, scaling, and outlier detection—was critical in optimizing model performance and minimizing overfitting. The results underscore the significant potential of machine learning for early cancer detection, offering healthcare professionals a reliable tool for precise and efficient diagnosis. This study's use of diverse performance metrics ensures a comprehensive evaluation, promoting data-driven approaches in modern healthcare.
