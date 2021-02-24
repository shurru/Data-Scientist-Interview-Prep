This section discusses some common data issues which are encountered when training a machine learning model, with potential solutions to overcome them. 

1. Unequal classes AKA class imbalance AKA unbalanced datasets

This is one of the more common issues encountered in data science, particularly in the medical field. In cases where a disease is not as prevalent or when data points are harder to collect due to the rarity of occurrence (eg. credit card fraud detection), you have to find other ways in which you can balance out your classification. 

* Resampling methods
Undersampling and oversampling from the class in which the data is lacking. 
- This can often be done by resampling from the dataset. 
- You could choose to randomly delete observations from the majority class and match the number of samples in the minority class.  
- You could alternatively choose to oversample from the minority class. This involves changing window-sizes in time-series data or generating synthetic data (think GANs) 
- <b> Bootstrapping </b> is also a resampling technique which can be used by sampling a dataset with replacement. This allows you to balance out the miniority class when training an algorithm. More info : https://machinelearningmastery.com/a-gentle-introduction-to-the-bootstrap-method
- 

* Class weights
When you encounter a skew in your dataset, providing different weights to your majority and minority classes allows you to train your model differently. It penalizes the misclassifications made in the minority class allowing you to have a less biased algorithm. 

Read more about class weights here: 

* Metrics of evaluation 
When working with imbalanced datsets, it's a better idea to evaluate the machine learning model on its precision(AKA positive predicitive value/PPV), recall (sensitivity) and specificity. 

![image]('/metrics.png')


