1. TF Hub is essentially a hub that has all these datasets that we can utilize to train our model. In "text classification of movie reviews", we got IMDB movie reviews from TF Hub in order to classify reviews as postive or negative. When we import tensorflow_datasets, this is basically a command that tells tensorflow to access the hub of datasets.

2. We used the binary_crossentropy loss function because this model is doing binary classification (classifying a review as either positive or negative). It's also benefical for dealing with probabilities. For the optomizer, we used "adam" again.

3. Loss is "error". Thus, as the number of epochs increases, you want to see training loss decrease because you want error to be decreasing as you train your model with more epochs. In this figure, as more epochs are run, training loss is decreasing. The validation loss "peaks" after 20 epochs, which indicateds overfitness - the model is training too well on the train data. 

[Graph 1](https://user-images.githubusercontent.com/60228374/87075502-735be180-c1ee-11ea-9c1d-3384b712cfc6.png)

4. In this graph, the training accuracy increases with each epoch. Validation accuracy peaks again, indicating overfitting.

[Graph 2](https://user-images.githubusercontent.com/60228374/87075885-03019000-c1ef-11ea-8248-b4d58a1dfb94.png)
