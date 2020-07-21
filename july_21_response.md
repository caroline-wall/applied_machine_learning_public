Premade estimators:

1. We split the labels from the training set by using the pop function to remove the target column from the dataset and set it to a new variable. In the original dataset, the column name was 'Species,' but we when we removed the column we renamed it 'train_y.'

2. DNNLinearCombinedClassifier: tf.estimator.DNNLinearCombinedClassifier()
   BoostedTreesEstimator: tf.estimator.BoostedTreesEstimator()
   BaselineEstimator: tf.estimator.BaselineEstimator()
   DNNEstimator: tf.estimator.DNNEstimator()
   Estimator: tf.estimator.Estimator()
   
3. Input functions supply the data for training and evaluating by creating a dictionary of the features and their corresponding values as well as an array containing the label for every data point. It then loads that data into a dataset. This is done in order to . Feature columns are definied in order to tell the model how to represent the data within each feature in the dictionary created earlier. 

4. Classifier.train() is calling the classifier function on the training data. We defined the classifier function previously. In this case, it is a DNNClassifier, which is used for deep models that perform multi-class classifications, which is appropriate as we are using three classes. The classifier initiates a DNNClassifier by building a DNN with two hidden layers with 30 and 10 nodes each, specified by the argument hidden_units. The feature columns are also passed in as well as the number of classes. Classifier.train() uses the nested function input_fn, which was previously defined as 

5. DNNClassifier: 0.900 84.7, 45.0, 68.9
