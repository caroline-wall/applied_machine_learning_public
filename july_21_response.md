# July 21, 2020 Response

Premade estimators:

1. We split the labels from the training set by using the pop function to remove the target column from the dataset and set it to a new variable. In the original dataset, the column name was 'Species,' but we when we removed the column we renamed it 'train_y.'

2. DNNLinearCombinedClassifier: tf.estimator.DNNLinearCombinedClassifier()\
   BoostedTreesEstimator: tf.estimator.BoostedTreesEstimator()\
   BaselineEstimator: tf.estimator.BaselineEstimator()\
   DNNEstimator: tf.estimator.DNNEstimator()\
   Estimator: tf.estimator.Estimator()
   
3. Input functions supply the data for training and evaluating by creating a dictionary of the features and their corresponding values as well as an array containing the label for every data point. It then loads that data into a dataset. This is done in order to separate the data into batches. Feature columns are definied in order to tell the model how to represent the data within each feature in the dictionary created earlier. 

4. Classifier.train() is calling the classifier function on the training data. We defined the classifier function previously. In this case, it is a DNNClassifier, which is used for deep models that perform multi-class classifications, which is appropriate as we are using three classes. The classifier initiates a DNNClassifier by building a DNN with two hidden layers with 30 and 10 nodes each, specified by the argument hidden_units. The feature columns are also passed in as well as the number of classes. Classifier.train() uses the nested function input_fn, which was previously defined as loading the data into a dataset and returning batches created from that dataset.

5. The LinearClassifier() performed the best with an accuracy of 96.7%.

   1. LinearClassifier()
   2. DNNClassifier()
   3. DNNLinearCombinedClassifier()

Linear model:

1. When comparing the histogram of age to the plot in which the relationship between age and itself is displayed, it becomes clear that the two are displaying the same shape, as both show the distribution of age within the dataset. The majority of passengers were in their late 20s.

<img width="625" alt="image" src="https://user-images.githubusercontent.com/67920492/88466829-630a5e80-ce9e-11ea-81d7-70523d86aa84.png">
<img width="325" alt="image" src="https://user-images.githubusercontent.com/67920492/88466750-9ac4d680-ce9d-11ea-8e02-87c8cc205494.png">

2. A categorical column is a column holding data that corresponds to a label, rather than having a numeric value. A dense feature stores data as a numpy array, meaning that categorical columns have to be encoded into numeric values.

3. The feature columns include sex, n_siblings_sposes, parch, class, deck, age, and fare. The first five are meant to be interpretated by the model as categorical, while the other two are to be interpretated as numerical. The initial output had an accuracy of 75.8%, making it an okay model. Adding a cross featured column makes the model more specific by exploring how the intersection of different features plays a role in determining whether or not a passenger survived. It could make the model more accurate by finding more specific correlations, which it does in this case as the accuracy increased to 77.6% when the interaction between age and gender was incorporated.

The predicted probabilities plot shows that the model more frequently predicted that a passenger would 
