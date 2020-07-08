1.  A) The training set is the data that is being fed into the neural network, to help the model "learn". The testing set is the data the model uses to asess its performance, through prediciting values based off of it. Thus, there is a training set and a testing set.

    B) Because there are 10 different types of numbers in the data set, there are 10 neurons to determine th eprobability that a number belongs to that class. The relu function takes a neuron that has an ouput less than zero, and sets it to zero. This is helpful because negative outputs are removed, that could skew data later on. The softmax function will take the prpbabilities of each number belonging to a certain class, find the largest one, and set it to 1.0. All the rest will be 0.0. This is benefifical because instead of looking for the highest value probability, you look for the 1.0. 
    
    C) The optomizer and loss function are used when compiling the model and the ones used, "adam" and "sparse_categorical_crossentropy" are useful when classifying multiple categories. 
    
    D) 1. The shape of the array training images is 28 x 28. 60,000 images in total. 
       2. The length of the training labels set is 60,000. 
       3. The shape of the array test images is also 28 x 28, with a total of 10,000 images.
       4. (wrote the code)
       5. 7 has the highest probability.
       6. (wrote the code)
