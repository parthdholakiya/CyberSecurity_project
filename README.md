# CyberSecurity_project


![Cyber-Security-Projects](https://user-images.githubusercontent.com/94167271/189382980-d379944b-732a-4d34-a789-a22dda748881.jpg)


Book-My-Show will enable the ads on their website, but they are also very cautious about their user privacy and information who visit their website. Some ads URL could contain a malicious link that can trick any recipient and lead to a malware installation, freezing the system as part of a ransomware attack or revealing sensitive information. Book-My-Show now wants to analyze that whether the particular URL is prone to phishing (malicious) or not.

Dataset Details: 

The input dataset contains an 11k sample corresponding to the 11k URL. Each sample contains 32 features that give a different and unique description of URL ranging from -1,0,1.

 1: Phishing

 0: Suspicious

 1: Legitimate

![image](https://user-images.githubusercontent.com/94167271/189637556-8cff5731-c127-4f7c-ba31-7034c2b3d237.png)

Found Favicol and PopUpwindow has Multicollinearity

multicollinearity and why it is a problem?

Multicollinearity exists whenever an independent variable is highly correlated with one or more of the other independent variables in a multiple regression equation. Multicollinearity is a problem because it undermines the statistical significance of an independent variable

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
### varaince : 0.03

