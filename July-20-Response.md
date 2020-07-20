A) In this exercise, we selected the RMSprop optimizer. The RMSprop is a good choice because it allows for an increased learning rate which allows the alogirthm to "take larget steps", and thus, converge faster! In RMSprop, the learning rate is adapted by dividing by the root of the sequared gradient. I think RMSprop is better for small batches in large datasets compared to other optimizers like adam.

B) The selected loss function is binary crossentropy. The loss function will return high values for bad predictions of binary classification, and low values for good predictions. 

C) In the code, when compiling the model, it says: metric = [accuracy]. Assigning this class creates 2 variables: total and count. Total is the number of times y_pred is equal to y_true in a binary classiication problem. In the end, total is divided by count to calculate frequency. 

D)  [Accuracy Graph](https://user-images.githubusercontent.com/60228374/87969168-a07e7e80-ca8f-11ea-9cfd-a57acf1f826c.png)

  [Loss Graph](https://user-images.githubusercontent.com/60228374/87969246-c3109780-ca8f-11ea-820c-ec9d27a6b100.png)
    
As epochs increased, validation loss increased while training loss increased - showing that the model may be overfit. With respect to accuracy, they both increased as epochs icnreased, and training accuracy was slightly higher which reveals the model is slightly overfit. Overall, I would say the model performed well. 
    
    
    
  Below, are the dog images I tested in the CNN. 
    
    
 ![Screen Shot 2020-07-20 at 5 22 35 PM](https://user-images.githubusercontent.com/60228374/87988382-3923f700-caae-11ea-9659-d91abcece374.png)
 
 - The model, was correct and classified this as a dog!
 
 ![Screen Shot 2020-07-20 at 5 30 30 PM](https://user-images.githubusercontent.com/60228374/87988669-b9e2f300-caae-11ea-9232-2b2a06daa584.png)
 
 - classified as a dog
 
 ![Screen Shot 2020-07-20 at 5 31 39 PM](https://user-images.githubusercontent.com/60228374/87988776-e0a12980-caae-11ea-9426-a383f74d7ee2.png)
 
 - I wanted to try this image, since this dog kind of looks like a cat! The model classified it as a cat 
 
 ![Screen Shot 2020-07-20 at 5 32 24 PM](https://user-images.githubusercontent.com/60228374/87988853-fc0c3480-caae-11ea-9f06-bd1856b3e952.png)

- classified as a cat

![Screen Shot 2020-07-20 at 5 33 08 PM](https://user-images.githubusercontent.com/60228374/87988900-16461280-caaf-11ea-9360-8c48e058fdf6.png)

- classified as a cat

![Screen Shot 2020-07-20 at 5 33 46 PM](https://user-images.githubusercontent.com/60228374/87988953-2c53d300-caaf-11ea-89d1-106188c925ee.png)

- classified as a cat
