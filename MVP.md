# Minimum Viable Product

### Background
Banks need deposits to make money. Which current customers are most likely to respond to a marketing campaign for a new product, and therefore put more money in the bank?

### MVP
Data is from [here](https://www.kaggle.com/rashmiranu/banking-dataset-classification?select=new_train.csv). Each row is one customer. The prediction value is whether the customer bought a product before; approximately 90% have not. 


One feature in the dataset is whether the customer has a home loan; one feature is whether the customer has a regular loan. I combined the two to make a total_products feature and fitted a logistic regression on that feature alone. The classifier predicted no one in the validation set would buy a product:

|              | Predicted No | Predicted Yes |
|----------    |--------------|---------------|
|**Actual No** | 5,706        | 0             |
|**Actual Yes**|   725        | 0             |

We want to increase recall. We're okay catching some people who don't actually buy the product in our marketing campaign, given how small our previous campaign was (see next paragraph).

Another feature in the dataset concerns a previous marketing campaign; most of the customers (27,725 of 32,154) were not contacted during that campaign. Nonetheless I fitted a logistic regression on the results from the campaign. This classifier correctly predicts some customers in the validation set will buy a product: 

|              | Predicted No | Predicted Yes|
|---           |---           |---           |
|**Actual No** | 5,633        |  73          |
|**Actual Yes**|   581        | 144          |

*Recall* = 0.1986

We can still increase our recall.

Further exploration into recall looked at the class imbalance. Two quick class imbalance models were fitted. With all variables and no imbalance adjustment, recall is 0.341. With oversampling, recall goes up to 0.669. With SMOTE, recall drops to 0.434

While SMOTE is noted to be problematic because of the assumption of the separable, convex categories, there are two features of this dataset that excuse these assumptions: 
1. the non-yes points between the "yes" customers may be people who were not contacted in the other marketing campaign - that is "nonexistent" rather than "failure"
2. we have no evidence that marketing to people is correlated with them leaving from the bank; thus, the non-yes points between "yes" customers have not been demonstrated to be a detriment to our marketing campaigns

### To Do
- Spend a little more time with models to see if any are more predictive than appear
- Instatiate decision tree model
- Try model aggregation 
