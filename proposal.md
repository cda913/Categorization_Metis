# Predicting Restaurant Coupon Usage

### Question
Bars, coffee shops, and other restaurants want to increase their traffic. Will sending a coupon to people who are driving nearby help? If so, who should we send the coupons to? I will analyze [this data set](https://archive.ics.uci.edu/ml/datasets/in-vehicle+coupon+recommendation) to determine when people accept a coupon for 20% off an order. 

### Tools
I will use Pandas and Numpy to clean the data; sklearn for categorization modeling; and matplotlib, seaborn, and Tableau to display the data.

### Data
An individual sample is a single coupon sent to a potential customer. There are 25 features not including the target feature. A variety of features concern the customer ranging from current conditions such as destination and passengers in the car; through more general features such as the number of times s/he went to a coffee house in the last month; to stable features such as education. There are additional features such as time of day, distance the customer (driver) is from the restaurant in question, and when the coupon expires. Whether the coupon is accepted or not is the target feature.

### MVP
MVP will be a logistic regression of the number of times the driver has gone to the various types of restaurants in the past month on whether the coupon is accepted or not, including a confusion matrix of predicted values for the target feature.
