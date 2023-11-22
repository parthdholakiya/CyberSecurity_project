# Cybersecurity Project

This project focuses on building a cybersecurity model utilizing various techniques such as Exploratory Data Analysis (EDA), Multicollinearity analysis, Hypothesis testing, Principal Component Analysis (PCA), chi-square test, handling data imbalance using Synthetic Minority Over-sampling Technique (SMOTE), and implementing machine learning algorithms like Logistic Regression, Decision Trees, XGBoost, Random Forest, GridSearchCV, and K-Fold Cross-Validation.

## Overview

The goal of this cybersecurity project is to detect potentially harmful or malicious websites, safeguarding users from security threats like malware, viruses, and phishing scams. By implementing machine learning techniques, we aim to predict the security status of websites based on different features extracted from URLs.

## Table of Contents

1. [Exploratory Data Analysis (EDA)](#eda)
2. [Multicollinearity Analysis](#multicollinearity)
3. [Hypothesis Testing](#hypothesis-testing)
4. [Principal Component Analysis (PCA)](#pca)
5. [Handling Data Imbalance with SMOTE](#smote)
6. [Machine Learning Algorithms](#machine-learning-algorithms)
   - Logistic Regression
   - Decision Trees
   - XGBoost
   - Random Forest
7. [GridSearchCV for Hyperparameter Tuning](#gridsearchcv)
8. [Receiver Operating Characteristic (ROC) Curve](#roc-curve)
9. [K-Fold Cross-Validation](#k-fold-cross-validation)
10. [Conclusion](#conclusion)

## 1. Exploratory Data Analysis (EDA) <a name="eda"></a>

In the initial stage, we perform Exploratory Data Analysis to understand the dataset's characteristics and gain insights into the distribution of features.

## 2. Multicollinearity Analysis <a name="multicollinearity"></a>

Identifying and addressing multicollinearity, especially between features like Pop Up Window and Favicon, to ensure stable and reliable regression coefficients.

## 3. Hypothesis Testing <a name="hypothesis-testing"></a>

Utilizing statistical hypothesis testing to make inferences about the population based on sample data and assess the significance of relationships between variables.

## 4. Principal Component Analysis (PCA) <a name="pca"></a>

Implementing PCA for dimensionality reduction to identify patterns and represent the dataset in a lower-dimensional space while retaining crucial information.

## 5. Handling Data Imbalance with SMOTE <a name="smote"></a>

Addressing data imbalance using Synthetic Minority Over-sampling Technique (SMOTE) to generate synthetic samples for the minority class, improving model performance.

## 6. Machine Learning Algorithms <a name="machine-learning-algorithms"></a>

Applying various supervised machine learning algorithms to train models on labeled data, including:
   - **Logistic Regression**
   - **Decision Trees**
   - **XGBoost**
   - **Random Forest**

## 7. GridSearchCV for Hyperparameter Tuning <a name="gridsearchcv"></a>

Implementing Grid Search to fine-tune hyperparameters for model optimization and improved performance.

## 8. Receiver Operating Characteristic (ROC) Curve <a name="roc-curve"></a>

Visualizing the performance of the binary classification model through an ROC curve, providing insights into the trade-off between true positive rate and false positive rate.

## 9. K-Fold Cross-Validation <a name="k-fold-cross-validation"></a>

Evaluating the model's performance using K-Fold Cross-Validation to mitigate overfitting and provide a robust estimate of accuracy.

## 10. Conclusion <a name="conclusion"></a>

In conclusion, this cybersecurity project employs a comprehensive approach, combining statistical analyses, machine learning algorithms, and validation techniques. The final model demonstrates a testing accuracy of 97%, showcasing its effectiveness in identifying and classifying potentially harmful websites.

Feel free to explore the code and contribute to the exciting field of cybersecurity.

---

*Note: Adjust the content and sections based on your specific project details.*



# CyberSecurity_project

![image](https://user-images.githubusercontent.com/94167271/234273272-bc0a0b68-c079-4d9d-a684-085b5c258a0a.png)

Book-My-Show will enable the ads on their website, but they are also very cautious about their user privacy and information who visit their website. Some ads URL could contain a malicious link that can trick any recipient and lead to a malware installation, freezing the system as part of a ransomware attack or revealing sensitive information. Book-My-Show now wants to analyze that whether the particular URL is prone to phishing (malicious) or not.

![Cyber-Security-Projects](https://user-images.githubusercontent.com/94167271/189382980-d379944b-732a-4d34-a789-a22dda748881.jpg)

Dataset Details: 

The input dataset contains an 11k sample corresponding to the 11k URL. Each sample contains 32 features that give a different and unique description of URL ranging from -1,0,1.

 1: Phishing

 0: Suspicious

 1: Legitimate

![image](https://user-images.githubusercontent.com/94167271/189637556-8cff5731-c127-4f7c-ba31-7034c2b3d237.png)

Found Favicol and PopUpwindow has Multicollinearity

multicollinearity and why it is a problem?

Multicollinearity exists whenever an independent variable is highly correlated with one or more of the other independent variables in a multiple regression equation. Multicollinearity is a problem because it undermines the statistical significance of an independent variable

#### Hypothesis testing

Hypothesis testing is a form of statistical inference that uses data from a sample to draw conclusions about a population parameter or a population probability distribution. First, a tentative assumption is made about the parameter or distribution. This assumption is called the null hypothesis and is denoted by H0. An alternative hypothesis (denoted Ha), which is the opposite of what is stated in the null hypothesis, is then defined. The hypothesis-testing procedure involves using sample data to determine whether or not H0 can be rejected. If H0 is rejected, the statistical conclusion is that the alternative hypothesis Ha is true.

### From chi-square test  found, popUpWidnow and Favicon has Multicollinearity

             Ho: popUpWidnow is independent of Favicon
             ha: popUpWidnow is Favicon dependent -> Multicollinearity

p_value of chi-square test is : 0.0
---------------------------------------------------------
Reject Ho, popUpWidnow is Favicon dependent -> Multicollinearity

PCA (Principal Component Analysis) takes advantage of multicollinearity and combines the highly correlated variables into a set of uncorrelated variables. Therefore, PCA can effectively eliminate multicollinearity between features.

### Applied PCA to solve multicollinearity

Here 1=55% and 0=44% found slightly unbalance data so use SMOTE for data balance.

After attempting SMOTE on train data.

![image](https://user-images.githubusercontent.com/94167271/189640166-616133a7-a18f-4369-8bfe-e2c797984fe1.png)

Implemented ML Algorithms for binary classification

        LogisticRegression

        DecisionTreeClassifier

        RandomForestClassifier

        XGBClassifier

        AdaBoostClassifier

### XGBClassifier gives Highest recall on Test data.
### after implementing Hyperparameter tuning on Xgboost using GridSearchCV recall reach up to 97 %.

### AUC on test data
![image](https://user-images.githubusercontent.com/94167271/189651768-58055b7d-5eb6-4eb3-8b3d-65cdb43c89c4.png)

### K-Fold cross-validation

### mean accuracy of xgb_hyper model is :  0.97
### variance  : 0.03


