# Breast-cancer-ml
This repository contains the work of A comparitive study of machine learning models on breast cancer part of our course work at University of Hertfordshire

Table of Contents
1.	Project Overview
2.	Objectives
3.	Dataset
4.	Exploratory Data analysis
5.	Data Preprocssing
6.	Model
7.	Results
8.	Conclusion

Project overview
This is an individual project on breast cancer analysis and there is a comparitive study between different models.The models used were logistic regression, Random forest an XG boost by considering various features of these models.

Objectives
1. To develop a machine learning model that can accurately classify breast tumours as benign or malignant based on diagnostic imaging data. 
2. To reduce the feature space while preserving important diagnostic data by using dimensionality reduction techniques, such PCA.
3. To evaluate and compare the performance of multiple machine learning models (Random Forest, XGBoost, and Logistic Regression) using crucial measures such as F1-score, precision, recall, and AUC-ROC. 
4. To choose the top-performing model for clinical usage while taking interpretability and generalisation into account, based on the major accuracy metric (AUC-ROC).
   
 Dataset
 
The Breast Cancer Wisconsin (Original) dataset, which was used in this study, is available through the UCI Machine Learning Repository at https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic and the data file is accessible https://archive.ics.uci.edu/static/public/17/data.csv under a Creative Commons (CC) license (Wolberg, W., 1990).
The UCI Machine Learning Repository, a popular resource for breast cancer prediction challenges, provided the dataset used in this investigation. Digital images of breast mass fine needle aspirations (FNA) are used to generate its diagnostic features. The dataset is a binary classification problem since each record represents a tumour that has been categorised as either benign or malignant. There is a little class imbalance in the dataset, which consists of 569 cases (357 benign and 212 malignant). This distribution reflects clinical difficulties in the actual world, where it is crucial to identify malignant cases, which are less common. Thirty numerical features that were taken from the images' cell nuclei are included in the collection. These characteristics include metrics like area, perimeter, smoothness, symmetry, compactness, concavity, texture.

Exploratary Data Analysis

Exploratory Data Analysis (EDA) involves a thorough analysis of a dataset to identify target labels and class imbalances. The process begins with a structural overview, revealing a minor imbalance in class labels. The EDA method uses bar charts to visualize the distribution of class labels, followed by descriptive statistics and correlation heatmaps to highlight connections between features. The next stage involves visual examination of specific features to determine their function in differentiating between benign and malignant tumours. boxplots, histograms, kernel density plots, and scatter plots help identify characteristics with greater classificational influence. The EDA process also involves analysing the target class distribution, feature data types, and feature descriptions to understand the dataset and determine the appropriate preprocessing methods. This process ultimately leads to more reliable and accurate predictive models.

The target class distrubution shows the class imbalance between the benign and malignant. The difference in the number of instances is depicted in the EDA.

The frequency distribution of the "Radius1" feature, a continuous variable in the dataset, is shown graphically by the bar plot. It draws attention to the data's variability, central tendency, and spread. An overlaying density curve provides further information about the distribution pattern.
The pair plot uses different colours (blue for benign and red for malignant) to emphasise the target variable, diagnosis, and shows the relationships and distributions of a few chosen parameters from the dataset (radius1, texture1, perimeter1, area1).

Finding trends, connections, and overlaps between the two target groups is made easier with the help of this visualisation. For instance, for most features, red (malignant) points are grouped around larger values, suggesting that greater values could be linked to malignancy. In a similar vein, certain traits' obvious separability points to their significance in classification tasks. With colour intensity signifying the degree and direction of correlations, the correlation heatmap offers a visual depiction of the relationships among the dataset's elements. Strong negative correlations (values near -1) are indicated by dark blue shades, and strong positive correlations (values near +1) are represented by dark red hues. Redundancy is suggested by features such as radius1, perimeter1, and area1, which exhibit substantial positive relationships with one another. In datasets where features represent related measures, this redundancy is typical. However, variables such as smoothness1 and fractal_dimension1 show lesser relationships with other features, suggesting that they may contribute unique information.

Preprocessing

Data cleansing and finding the missing values were done as part of preprocessing. Imputation is not necessary because the dataset from the UCI repository is clean and devoid of missing values.This result was drawn following a Null Value Check that verified all features had zero missing values using routines like sum() and isnull().

Detecting outliers help to improve the accuracy and precision the Z-score method is used for finding the outliers and removing the outliers.

Standardisation: By bringing features to a common scale, this strategy is especially useful for algorithms that are sensitive to feature magnitudes. Models like logistic regression benefit greatly from standard scaling, which employs zero mean and unit variance. 

Normalisation: However, normalisation, which entails scaling characteristics to a range between 0 and 1.
Principal Component Analysis (PCA): To reduce dimensionality while preserving variance, apply PCA after scaling. This process can improve model performance and processing efficiency by removing noise and multicollinearity.

Model
Three machine learning models are created and refined: Random Forest, XGBoost, and Logistic Regression. Performance criteria including F1-score, precision, recall, and AUC-ROC are used to assess these models; the main accuracy statistic is AUC-ROC. For clinical use, the model that best combines generalisation, interpretability, and accuracy is chosen.
Three models—XGBoost, Random Forest, and Logistic Regression—were assessed. With balanced precision, recall, and F1-scores for both classes, Logistic Regression demonstrated significant generalisation without overfitting, achieving a test accuracy of 93.75%. With a test accuracy of 91.96%, XGBoost performed better than the others and was particularly good at handling unbalanced data. These findings demonstrate machine learning's promise as a dependable and expandable substitute for conventional diagnostic techniques, facilitating quicker and more precise treatment choices.

Model Assesment

I used multiple metrics, such as accuracy, precision, recall, F1-score, and ROC-AUC, to assess and improve the models. Accuracy quantified the total proportion of cases that were correctly classified, whereas precision focused on the ratio of true positives to all expected positives. The F1-score provided a balanced metric by computing the harmonic mean of precision and recall, whereas recall focused on the ratio of true positives to all actual positives.The models' discriminating power over a range of categorisation thresholds was measured using the ROC-AUC score. 
By means of methodical preparation, model implementation, and optimisation, I created a strong framework for predicting breast cancer.

Conclusion

This study developed an effective breast cancer prediction system by utilising cutting-edge machine learning methods, such as Random Forest, XGBoost, and Logistic Regression. In order to maximise model performance and minimise overfitting, thorough data preprocessing—which includes feature selection, scaling, and outlier detection—was essential. The results highlight machine learning's enormous potential for early cancer detection and give doctors a trustworthy tool for precise and effective diagnosis. The study's use of a variety of performance criteria made for a thorough assessment, highlighting the models' adaptability and their role in promoting data-driven approaches in contemporary healthcare.
