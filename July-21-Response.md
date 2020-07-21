A) 1. To split the labels from the trianing set, we used the code: train_y = train.pop('Species'). We did the same for the testing dataset, because we do not want the label data to be with the feature data. The name of the labels dataset is 'SPECIES'.

   2. tf.estimator.LinearRegressor()- an estimator that trains a linear regression model
      tf.estimator.DNNClassifier() - classifier for DNN models
      tf.estimator.DNNRegressor()- regressor for DNN models
      tf.estimator.BaselineClassifier()- classifier that establishes a simple baseline, predicts probability distirbution of classes/labels
      tf.estimator.BoostedTreesClassifier()- classifier for boosted tree models
      
   3. You must write the input functions and defining the feature colums, if you are writing aprogram absed on pre-made estimators. Input functions are necessary for supplying the data to the estimator for evaluation/training. It is a function which returns the object, a 2 element tuple. It has a "features" dictionary, and a label" list. The feature column is necessary to tell the model how to use the data from the features dictionary. When using an estimator, you pass it the list of feature columns you want to use. 
   
   4. Classifier.train() is training the model further. The nested function is input_fn(). We created the command, because we want to call upon it. 
   
   5.
   
B) 1. Below, I used the seaborn library to produce a pairplot of a couple features. I also created a histogram of the age distribution on board. 

![Figure_1](https://user-images.githubusercontent.com/60228374/88090838-2b2caf80-cb5c-11ea-9acf-60324b69cd0b.png)
![Figure_2](https://user-images.githubusercontent.com/60228374/88091045-7d6dd080-cb5c-11ea-8786-6caf2dcb0da3.png)

   The histogram for age looks very similar to the plot for the feature age. Both have the same peaks and distirution. My paiplot seems to be a little cut off, but the distirbution of age is on the top, left of the pairplot. It's clear from the plot that the average age of people on board was between 20-30 years old. 
 
   2. 
