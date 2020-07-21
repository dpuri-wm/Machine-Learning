A) 1. To split the labels from the trianing set, we used the code: train_y = train.pop('Species'). We did the same for the testing dataset, because we do not want the label data to be with the feature data. The name of the labels dataset is 'SPECIES'.

   2. tf.estimator.LinearRegressor()- an estimator that trains a linear regression model
      tf.estimator.DNNClassifier() - classifier for DNN models
      tf.estimator.DNNRegressor()- regressor for DNN models
      tf.estimator.BaselineClassifier()- classifier that establishes a simple baseline, predicts probability distirbution of classes/labels
      tf.estimator.BoostedTreesClassifier()- classifier for boosted tree models
      
   3. You must write the input functions and defining the feature colums, if you are writing aprogram absed on pre-made estimators. Input functions are necessary for supplying the data to the estimator for evaluation/training. It is a function which returns the object, a 2 element tuple. It has a "features" dictionary, and a label" list. The feature column is necessary to tell the model how to use the data from the features dictionary. When using an estimator, you pass it the list of feature columns you want to use. 
   
   4. Classifier.train() is training the model further. The nested function is input_fn(). We created the command, because we want to call upon it. 
   
   5.
   
B) 1. Below, I used the seaborn library to produce a pairplot of a couple features. 

![Figure_1](https://user-images.githubusercontent.com/60228374/88090838-2b2caf80-cb5c-11ea-9acf-60324b69cd0b.png)
 
   2. 
