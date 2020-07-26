## Project assignment

The goal of this project was to determine population counts of the Korle Gonno neighborhood in Accra, through specifying and estimating a model. Data consisted of 10,000 bird's eye images of the location, with each image having a size of 480 x 480 pixels. Another file contained the counts of all persons estimated to reside within the area at the time the images were taken, September 2005. An example image from the dataset is shown below:

![9029](https://user-images.githubusercontent.com/60228374/88491393-653ced80-cf70-11ea-8f01-9ceb4c03d351.jpeg)


## Creation of the model

The general structure of how I completed this assignment is as follows: 

- Split the data into two datasets, train_imgs and test_imgs 
  - I split 90% of the data into the training folder and 10% of the data into the testing folder
  - I physically split the images on my desktop into 2 folders, then created a path for each, which is how I "called" upon them in pycharms
- Create a neural network 
- Compile the model
- Fit the model on the training data

I began by creating a simple Dense Neural Network, as a "toy model". I included 3 dense layers that had 64,64, and 1 neuron(s). The optimizer used was RMSprop, and the loss function used was 'mse' - mean square error, as population counts are continuous. I fit my training data on the DNN, and due to the capabilites of my laptop, I was only able to fit the DNN on 1,000 images, with a batch_size = 50 and steps_per_epoch = 20. My mean square error/loss was very high, even after running three epochs. However, this is okay because the DNN is not the model I intended to use on my assingment. I needed a more robust machine learning model that would be better for identifying the relationship between urban form and population. I decided to choose a convolutional neural network. 

After playing around with convolutional layers and the neurons, along with balancing the processing capabilites of my 2012 macbook air, my model consisted of 2 Conv2D layers (64 and 32 neurons), 2 MaxPooling2D layers, 1 Flatten() layer, and 2 Dense layers (64 and 1 neurons). Unfortunately, I have having lots of technical issues, and thus, was only able to fit 100 training images into my CNN. My final loss, after 3 epochs, was a MSE of 1231. Although this is high, I do believe I could lower the loss and error if my laptop were able to handle more convolutional layers, and if the CNN was able to be fitted on all 9000 training images. Below, I grapphed loss (mse), and mean absolute error over the three epochs. 

![better1](https://user-images.githubusercontent.com/60228374/88491701-f6ad5f00-cf72-11ea-8dff-9a144b70c314.png)
![better2](https://user-images.githubusercontent.com/60228374/88491734-4be97080-cf73-11ea-815e-abc596d1174e.png)

As seen from the graphs, both mean square error and mean absolute error, on average, decreased over the course of the training epochs. 

## Conclusion

In general, it's easy to see that my model was highly inaccurate. I would have loved to fit the model on more trianing images and add more convolutions to my neural network. This was definitly an interesting project, and it has useful applications. For example, this project has taught me how convolutional neural networks can be useful in population estimation. In DATA 150 last semester, I read various articles about how surveillance technology can estimate population counts, and it was beyond fascinating to see that actually put into action with this project. I am now aware of the technique and a little of the mathematics behind it. 
