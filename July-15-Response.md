The ImageDataGenerator() command is essentially reading the pictures from our source folder. It reads images from subdirectories and automtically labels them from the name of the subdirectory. For example, the training directory will have a horses and a humans subdirectory within it, and the ImageGenerator will label those images within them. The only argument ImageDataGenerator() takes is to rescale the data. Inside the paranthesis, we write "rescale = 1/255". As the lab says, the ImageDataGenerator allows us to instantaniate generators of image batches, like the train_generator or validation_generator. Those generators utilize the ImageDataGenerator() command to flow images in. To flow in images to the generated object, a few parameters are required: the directory must be specified, a target size, batch size, and class mode. The target size indicates the size of the image that will be fed into the CNN. 


- train_datagen = ImageDataGenerator(rescale=1/255)
- train_generator = train_datagen.flow_from_directory(
        '/tmp/horse-or-human/',  
        target_size=(300, 300),  
        batch_size=128,
        class_mode='binary')
        
The two lines of code above show how the ImageDataGenerator works, "called upon" by the variable train_datagen. When creating the generated object, train_generator, we use the command "train_datagen.flow_from_directory(). 
