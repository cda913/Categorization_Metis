### Abstract
A bank wants to increase revenue by marketing a long term product to customers. I have access to some details about the customers and the results from a previous marketing campaign. Less than 10% of the customers responded positively to the campaign; however, most of the customers were not contacted. Given the number of people were not contacted, I chose recall as the evaluation metric. I tried several learning algorithms, and determined that a random forest with an adjusted threshold gave the best results in terms of recall. 

### Design
This project originates from the Kaggle dataset [Banking Dataset Classification](https://www.kaggle.com/rashmiranu/banking-dataset-classification?select=new_train.csv). The data is provided from a Portuguese bank and contains customers and the results from the previous marketing campaign. Determining which customers are most likely to respond to a future marketing campaign will increase the bank’s revenue. I decided to focus on recall because the previous marketing campaign was directed at only 14% of the customers. 
### Data
The data consists of 32,950 customers with 15 features, 10 of which are categorical. Features were surprisingly spare for a banking data set: for example, there were no features concerning income.
### Algorithms
_Feature engineering_
- converting categorical variables to dummy variables
- dropping unnecessary features
- testing various combinations of features

_Models_
- logistic regression
- decision trees
- random forests
- balanced bagging classifiers
A random forest with a threshold of approximately 17% produced the best recall 

_Model Evaluation and Selection_

The whole data set was split into 60/20/20 train vs. validation vs. test/holdout. Models were evaluated either on the 20% validation, or  with 5-fold cross validation on the 80% training/validation portion. As stated above, the metric used for evaluation was recall. A change in threshold proved to be more productive than weighting the uneven minority class.  

_Results_

Recall on the holdout test set was 98%. The confusion matrix was: 
|   | Predicted No | Predicted Yes|
|---|---|---|
|**Actual No** | 26 |5680|
|**Actual Yes**|   4  |721|

The high number of false positives is acceptable because of the high number of people who were not targeted in the prior campaign.

### Tools
- Numpy and Pandas for data manipulation
- Scikit-learn and imblearn for modeling
- Matplotlib and Seaborn for visualizations
### Communication
PowerPoint presentation

