# Impact of Dimensionally Reduction Method on Non-Linear Classifier Performance

## Background Study and Aim

This study aims to discover a suitable combination of contemporary dimensionally reduction techniques and robust non-linear prediction classifier as such to examine the impact of the dimensionally reduction method on the classifier performance.

## Methodology

This study used the popular methodology of data mining called cross-industry standard process for data mining (CRISP-DM) which contains 6 steps to make data mining model useful for decision making.

### Dataset Description

Dataset used is a bank marketing application, which is created by Paulo Cortez (Univ. Minho) and Sérgio Moro (ISCTE-IUL) in 2012. It was retrieved from [UCI Machine Learning Repository]. The scope of the data is only limited to a Portugese banking institution. The datasets are used to predict whether the customer will subscribe to the term deposit or not via the marketing campaigns. During the marketing campaigns, cold calls to customers will made by the bank workers and it can be a few times to the same customer to convince the customer to subscribe to the term deposit offered by the bank. The dataset contains 41188 instances and 21 attributes which includes the client’s demographics and socio-economic spectrum. The dataset contains numerical and categorical type of attributes while the target output is in categorical type as well. 

### Data preprocessing
The dataset was cleaned and pre-processed by removing outliers, missing values, and redundant features. The categorical features were encoded using label encoding, and the numerical features were normalized to have a range of 0 to 1. The dataset was split into train and test sets using stratification to preserve the class imbalance.

### Feature selection / dimensionality reduction
This study used two methods to reduce the dimensionality of the dataset: wrapper method and principal component analysis (PCA). The wrapper method used sequential feature selection with decision tree classifier as the estimator to select the best subset of features based on F1-score. The PCA method used the explained variance ratio to select the number of principal components that capture most of the variance in the data.

### Classification model
This study used decision tree as the non-linear classification model to predict whether the customer subscribed to a term deposit or not. The decision tree was constructed using the entropy criterion to measure the information gain at each node. The hyperparameters of the decision tree were set to max_depth = 5 and min_samples_leaf = 20. 


### Evaluation metrics
The study used accuracy, sensitivity, specificity, and F1-score to evaluate the performance of the classification model. The F1-score was considered the most relevant metric for the imbalanced dataset, as it is the harmonic mean of precision and recall.

## Results and discussions
### Comparison of dimensionality reduction methods
The results showed that the wrapper method outperformed the PCA method in terms of F1-score, precision, and recall, indicating that the wrapper method was able to select the most relevant features for the classification task. \
The wrapper method was more suitable for the customer-related dataset, which contained many irrelevant and highly correlated features. The wrapper method was able to remove the noise and find the minimum subset of features that capture the related attributes of the dataset. \
The PCA method, on the other hand, was a feature extraction approach that projected the data onto fewer principal components that explained the variance of the whole dataset, but did not necessarily preserve the information relevant for the classification task.

## Conclusion
As a conclusion, the feature selection using wrapper method worked better than the dimensionality reduction using PCA in the bank marketing dataset. The study suggested that a combination of wrapper method and decision tree classifier was a promising approach for predicting the client response rate for the term deposit scheme.
