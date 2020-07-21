A) 1. To split the labels from the trianing set, we used the code: train_y = train.pop('Species'). We did the same for the testing dataset, because we do not want the label data to be with the feature data. The name of the labels dataset is 'SPECIES'.

   2. tf.estimator.LinearRegressor()- an estimator that trains a linear regression model
      tf.estimator.DNNClassifier() - classifier for DNN models
      tf.estimator.DNNRegressor()- regressor for DNN models
      tf.estimator.BaselineClassifier()- classifier that establishes a simple baseline, predicts probability distirbution of classes/labels
      tf.estimator.BoostedTreesClassifier()- classifier for boosted tree models
      
   3. You must write the input functions and defining the feature colums, if you are writing aprogram absed on pre-made estimators. Input functions are necessary for supplying the data to the estimator for evaluation/training. It is a function which returns the object, a 2 element tuple. It has a "features" dictionary, and a label" list. The feature column is necessary to tell the model how to use the data from the features dictionary. When using an estimator, you pass it the list of feature columns you want to use. 
   
   4. Classifier.train() is training the model further. The nested function is input_fn(). We created the command, because we want to call upon it. 
   
   5. DNNClassifier - .767
   
      DNNLinearCombinedClassifier - .733
      
      LinearClassifier - .967
      
      The LinearClassifier performed best! However, I may have made a mistake. When searching the parameters that Linearclassifier accepted, I couldn't find an argument to enter the hidden layers of nodes of [30,10]. I'll look into this.
   
B) 1. Below, I used the seaborn library to produce a pairplot of a couple features. I also created a histogram of the age distribution on board. 

![Figure_1](https://user-images.githubusercontent.com/60228374/88090838-2b2caf80-cb5c-11ea-9acf-60324b69cd0b.png)
![Figure_2](https://user-images.githubusercontent.com/60228374/88091045-7d6dd080-cb5c-11ea-8786-6caf2dcb0da3.png)

   The histogram for age looks very similar to the plot for the feature age. Both have the same peaks and distirution. My paiplot seems to be a little cut off, but the distirbution of age is on the top, left of the pairplot. It's clear from the plot that the average age of people on board was between 20-30 years old. 
 
   2. A categorical column is a feature that involves non-numerical values, like the columns: "sex" or "deck". The values stored in these features are not numbers, like for example, male and female. A dense feature is a layer based on the supplied feature columns, and can be used to inspect the result of a feature column. 
   
   3. The model acheived 75% accuracy! To increase performance, we added a cross featured column, that captured the interaction between age and sex. This increased accuracy to 77.6%. I produced an ROC plot, receiver operating curve, and it shows the tradeoff between the true positive rate and false positive rate. Both increase over time. In the beginning, the true positive rate increased much faster than the false positive rate. However, as the model progressed, the rate of false positives increased. 

![Screen Shot 2020-07-21 at 4 47 03 PM](https://user-images.githubusercontent.com/60228374/88105382-d300a800-cb71-11ea-976d-607299afebbe.png)
