1. TF Hub is essentially a hub that has all these datasets that we can utilize to train our model. In "text classification of movie reviews", we got IMDB movie reviews from TF Hub in order to classify reviews as postive or negative. When we import tensorflow_datasets, this is basically a command that tells tensorflow to access the hub of datasets.

2. We used the binary_crossentropy loss function because this model is doing binary classification (classifying a review as either positive or negative). It's also benefical for dealing with probabilities. For the optomizer, we used "adam" again.

3. 
