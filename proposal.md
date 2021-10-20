# Predicting Bank Deposits

### Question
Banks need customers to make deposits in order to make money off the deposits, but not all customers are able to make larger deposits. Which customers are good ones to target in a marketing campaign advertising a new, high income product? Are any customers not good customers to target with a marketing campaign at all? I will analyze [this data set](https://www.kaggle.com/rashmiranu/banking-dataset-classification?select=new_train.csv) to determine which features are predictive of good customers to whom to target marketing of this new product. 

### Tools
I will use Pandas and Numpy to clean the data; sklearn for categorization modeling; and matplotlib, seaborn, and Tableau to display the data.

### Data
An individual sample is a single customer. There are 15 features not including the target feature, including information concerning the number of products the customer has with the bank and information about the previous marketing campaign. The target feature is whether the customer agreed to buy the new banking product.

### MVP
MVP will be a logistic regression of the number products the customer has with the bank on whether the customer agreed to buy the new product or not, including a confusion matrix of predicted values for the target feature.
