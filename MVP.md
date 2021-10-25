# Minimum Viable Product

### Background
Banks need deposits to make money. Which current customers are most likely to respond to a marketing campaign for a new product, and therefore put more money in the bank?

### MVP
Data is from [here](https://www.kaggle.com/rashmiranu/banking-dataset-classification?select=new_train.csv). Each row is one customer. The prediction value is whether the customer bought a product before; approximately 90% have not. 

One feature in the dataset is whether the customer has a home loan; one feature is whether the customer has a regular loan. I combined the two to make a total_products feature and ran a logistic regression. The classifier predicted no one would buy a product:

|          | Predicted No | Predicted Yes |
|----------|--------------|---------------|
|**Actual No** | 5,706        | 0             |
|**Actual Yes**|   725        | 0             |

