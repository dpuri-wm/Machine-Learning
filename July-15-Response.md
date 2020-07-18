A) The ImageDataGenerator() command is essentially reading the pictures from our source folder. It reads images from subdirectories and automtically labels them from the name of the subdirectory. For example, the training directory will have a horses and a humans subdirectory within it, and the ImageGenerator will label those images within them. The only argument ImageDataGenerator() takes is to rescale the data. Inside the paranthesis, we write "rescale = 1/255". As the lab says, the ImageDataGenerator allows us to instantaniate generators of image batches, like the train_generator or validation_generator. Those generators utilize the ImageDataGenerator() command to flow images in. To flow in images to the generated object, a few parameters are required: the directory must be specified, a target size, batch size, and class mode. The target size indicates the size of the image that will be fed into the CNN. 


- train_datagen = ImageDataGenerator(rescale=1/255)
- train_generator = train_datagen.flow_from_directory(
        '/tmp/horse-or-human/',  
        target_size=(300, 300),  
        batch_size=128,
        class_mode='binary')
        
The two lines of code above show how the ImageDataGenerator works, "called upon" by the variable train_datagen. When creating the generated object, train_generator, we use the command "train_datagen.flow_from_directory(). For class mode, consider whether its a binary classification or not. In our case, we are classifying between 2 things: horses and humans. Thus, it is a binary classification and we use "binary" as the class mode. In the train generator and validation generator, one parameter that is different when using the .flow_from_directory() command is the batch size. The batch size is much smaller in the validation egenrator, because we need fewer images for validation of the model. 

B) The pair plot allows us to see the relationship between different features in the dataset. For example, from the plot I can determine that there is a positive correlation between weight and displacement. The diagonal axis is just the distribution of that variable. 

[pairplot](https://user-images.githubusercontent.com/60228374/87839650-d2160080-c869-11ea-9cc8-66241d0ce1fa.png)

When observing the hist.tail(), the model does seem to improve beacuse MSE decreases. However, its interesting because MAE increases on the other hand. I'm not sure if this means the model is increasing or decreasing in accuracy...

[hist.tail()](https://user-images.githubusercontent.com/60228374/87839669-e528d080-c869-11ea-81ee-655f13f7b45a.png)

C) The graph below shows the differences made in constructing each model and the underfitting/overfitting of each. The tiny model is the most underfit, which makes sense because the model does not have as many parameters to "learn" upon. The large model was the most overfit, because the model has so many parameters to learn. The medium model is probably the best choice for the data. 

[model overfitting/underfitting](https://user-images.githubusercontent.com/60228374/87839715-14d7d880-c86a-11ea-864b-167b75d4b6f1.png)
