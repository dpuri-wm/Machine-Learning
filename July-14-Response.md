A) I played around with different filters, and ended up applying the following filter to the image three times: filter = [[-2,0,-2],[0,0,0],[2,0,2]]. Below, is the original image, followed by each time I applied the filter to the image. 

- [Originial image](https://user-images.githubusercontent.com/60228374/87457111-df1ac180-c5d5-11ea-84a5-c858df07fdbf.png)

- [Filter applied #1](https://user-images.githubusercontent.com/60228374/87457244-0c676f80-c5d6-11ea-9804-a2151d697ab5.png)

- [Filter applied #2](https://user-images.githubusercontent.com/60228374/87457318-27d27a80-c5d6-11ea-8e2a-240d8731ab30.png)

- [Filter applied #3](https://user-images.githubusercontent.com/60228374/87457361-3c167780-c5d6-11ea-8436-ce8710b7981a.png)

There is a big difference in the image when I applied the filter for the first time, as the image turned much darker and vertical lines became much more pronounced. As I applied the filter twice more, the differences between the images became much more subtle. However, I could still see somehwat of a difference each time the filter was applied. White lines became brighter and more pronounced. I think I am functionally accomplishing multiplying each pixel by the filter weight manually. I think this application is important for computer vision in general, because the computer should be able to contrast the image and make some lines more pronounced - to allow for better recognition of pictures within the image. In basic language, a filter allows the computer to cut out what's not important, and keep what's important for classification.

B) I pooled the convoluted image with a 2x2 filter. Below is the result!

- [2X2 Filter applied](https://user-images.githubusercontent.com/60228374/87458190-99f78f00-c5d7-11ea-84ad-7c60f4455929.png)

The image is now 1/4 of its actual size; thus, the result decreased in size. All the features of the image are mantained, but I do think that the image looks just a little bit "grainy" to me.The white lines are a little thicker. This type of pooling is called MAX pooling - we iterate over the image and all the pixels, look at a pixel and its immediate neighbors, and take the largest of them and load it into the image. 

C) When I used a Dense Neural Network (DNN) on the mnist (handwritten letters) dataset, I received an accuracy of .9760, and a loss of 0.0807. 97% accuracy is very good, but I thought I could get it ot imporve with a convoluted neural network (CNN). The CNN took much longer to run, but it improved the accuracy by a lot! I got an accuracy of .9906, and a loss of .0275. I think it's safe to say that the convolutions improved the performance of my model. I plotted the convolutions graphically, and attached them below! When I ran the CNN with a filter size of 16, compared to 64, and my run-time for each epoch decreased dramatically! With 64, I had a runtime of about 90-100 seconds for each epoch, but it reduced to around 25 seconds for each epoch with a filter size of 16. My accuracy also slightly increased.

- [Plotted Convolutions](https://user-images.githubusercontent.com/60228374/87461255-2a37d300-c5dc-11ea-8cc1-3ce92eb891c0.png)



