# Breast-Cancer-Diagnosis-Using-Machine-Learning
In this project, I am using the University of Wisconsin's opensource dataset on breast cancer to classify malignant and benign samples using PyCaret

# Dataset:
Breast Cancer Wisconsin (Diagnostic) Data Set
Link:- https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

# Dataset Contents:
* 33 columns - 31 useful (Dropped:- Id, Unnamed: 32)
* 569 rows - 350+(B) and 200+(M)
* Target - diagnosis column (categorical)

# Steps Followed and Observations:
* Importing the libraries and dataset
* Exploring the dataset and analysis
* Upsampling using SMOTETomek to handle the class-imbalance
* Found outliers in almost all numerical columns but didn't remove since 23% of the data will be lost
* As per industry standards, 5-10% of the data can be removed as per usecase
* Upsampled data had 350 samples representing each class
* Pycaret was used to find the best performing model (automatically)
* Extra-Trees Classifier was found to be the accurate and precise model having highest AUC score
* Performed Hyper-Parameter Tuning, Model Saving, Evaluation and Prediction

# Outlier Removal Concept:
Data points that are only present within 3 standard deviations from the mean will be taken into consideration and others will be detected as outliers.

# Hybrid Upsampling Technique - SMOTE+TOMEL
"Hybridization techniques involve combining both undersampling and oversampling techniques. This is done to optimize the performance of classifier models for the samples created as part of these techniques.

SMOTE+TOMEK is such a hybrid technique that aims to clean overlapping data points for each of the classes distributed in sample space. After the oversampling is done by SMOTE, the class clusters may be invading each other’s space. As a result, the classifier model will be overfitting. Now, Tomek links are the opposite class paired samples that are the closest neighbors to each other. Therefore the majority of class observations from these links are removed as it is believed to increase the class separation near the decision boundaries. Now, to get better class clusters, Tomek links are applied to oversampled minority class samples done by SMOTE. Thus instead of removing the observations only from the majority class, we generally remove both the class observations from the Tomek links."                                                                                          
@Analytics Vidhya [1]

# Classification Report
![image](https://user-images.githubusercontent.com/106440078/213232043-36dd8460-6731-4a2c-a13e-812ef868ad65.png)


# Confusion Matrix
![image](https://user-images.githubusercontent.com/106440078/213231060-65475753-3368-4557-88f0-30f8b8694ddd.png)

# ROC Curve
![image](https://user-images.githubusercontent.com/106440078/213231128-0a7a3356-129b-4667-ad4c-434e0f0c8765.png)

# Precision-Recall Curve
![image](https://user-images.githubusercontent.com/106440078/213232219-911824bf-d913-4ee9-8425-bb34acad40db.png)

# Validation Curve
![image](https://user-images.githubusercontent.com/106440078/213232293-a3671d44-42e5-4357-8add-aa9bd9f4ba8b.png)

# Feature Importance Plot
![image](https://user-images.githubusercontent.com/106440078/213231703-020de2e8-ddbf-4675-8c87-271867086232.png)

# Decision Boundary
![image](https://user-images.githubusercontent.com/106440078/213231864-dcf39e64-faf9-4372-b5e0-2c5b3247d138.png)

# Reference:
[1] https://www.analyticsvidhya.com/blog/2020/10/overcoming-class-imbalance-using-smote-techniques/
