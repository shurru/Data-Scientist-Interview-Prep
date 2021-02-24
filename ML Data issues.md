This section discusses some common data issues which are encountered when training a machine learning model, with potential solutions to overcome them. 

1. <b>Unequal classes AKA class imbalance AKA unbalanced datasets </b>

This is one of the more common issues encountered in data science, particularly in the medical field. In cases where a disease is not as prevalent or when data points are harder to collect due to the rarity of occurrence (eg. credit card fraud detection), you have to find other ways in which you can balance out your classification. 

* <b> Resampling methods: </b> 
<i>Undersampling and oversampling from the class in which the data is lacking.</i>
  - This can often be done by resampling from the dataset. 
  - You could choose to randomly delete observations from the majority class and match the number of samples in the minority class.  
  - You could alternatively choose to oversample from the minority class. This involves changing window-sizes in time-series data or generating synthetic data (think GANs) 
  - <b> Bootstrapping </b> is also a resampling technique which can be used by sampling a dataset with replacement. This allows you to balance out the miniority class when training an algorithm. More info : https://machinelearningmastery.com/a-gentle-introduction-to-the-bootstrap-method


* <b>Class weights</b>
  - When you encounter a skew in your dataset, providing different weights to your majority and minority classes allows you to train your model differently. 
  - It penalizes the misclassifications made in the minority class allowing you to have a less biased algorithm. 
  - Read more about class weights here: https://www.analyticsvidhya.com/blog/2020/10/improve-class-imbalance-class-weights/

* <b>Metrics of evaluation </b>
  - When working with imbalanced datsets, it's a better idea to evaluate the machine learning model on its precision(AKA positive predicitive value/PPV), recall (sensitivity) and specificity. 
  - You can also calculate the F-score which allows an understanding of the tradeoff between precision and recall
  - Investigating the ROC curve and Area under curve (AUC-ROC) also visualize the algorithms' ability to discrimate the positive class from the rest of the data.   The AUC-ROC is a single-value metric which summarizes the quality of a classifier.

![image](https://github.com/shurru/Data-Scientist-Interview-Prep/blob/main/MLmetrics.png=200x)


2. <b> Small Dataset Size </b>

One of the most common issues I've encountered over my experience with niche healthcare issues are that dataset sizes are often quite small. While it is true that large datasets are greatly beneficial to train a machine learning algorithm, there are ways to use smaller datasets. Additionally, small datasets often lead to overfitting of a machine learning model. Some tips and tricks: 

* Using simpler models (regression or kNN is good) 
* Use regularization techniques such as L1 and L2 norms which make models more conservative
* Be wary of outliers : any outliers tend to confuse the model and determine irrelevant patterns
* Data Augmentation 
  - In the case of image data, augmentation is often done through transformations such as : 
    - rotation of the image
    - changing it to grayscale
    - zooming in
    - changing brightness, etc.
  - You can read more about this on: https://machinelearningmastery.com/how-to-configure-image-data-augmentation-when-training-deep-learning-neural-networks/

  - In the case of numeric data use it's possible to use the resampling techniques described above 
  
* Transfer Learning
  - Like the name suggests, transfer learning refers to using the learning from one task to apply to another (similar) task. 
  - This often involves the use of deep learning networks such as Convolutional Neural Networks wherein the inital layers are quite generalized and the deeper layers contain information about the specific problem. 
  - Since the lower layers features are still relevant, we only need to make changes to the higher layers. 

Read more on: https://towardsdatascience.com/breaking-the-curse-of-small-data-sets-in-machine-learning-part-2-894aa45277f4

