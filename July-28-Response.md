1. One-hot encoding is very inefficient because it is a sparse vector - meaning that most indeces are 0. This just wouldn't make sense efficiency wise, if for example, there were 10,000 words in the vocabulary. To one-hot encode a word, 99.99% of the indeces would be 0 and just one would have 1 stored in it. In comparison, word embeddings are efficient, dense representations. A dense vector is one where all elements are full. For example, "the cat sat on the mat" could have a dense vector of [5,1,4,3,5,2]. An embedding is a dense vector of floating point values - these values are trainable parameters/ weights learned by the model during training. After the weights are learend, you can encode each word by looking at the dense vector it corresponds to. 

2. ![Screen Shot 2020-07-28 at 2 18 35 PM](https://user-images.githubusercontent.com/60228374/88705266-4871f880-d0dd-11ea-88b1-49657ad000e5.png)
![Screen Shot 2020-07-28 at 2 18 46 PM](https://user-images.githubusercontent.com/60228374/88705273-4a3bbc00-d0dd-11ea-83d9-7d41b027b2fe.png)

Above are the two plots from the word embedding tensorflow exercise. Training accuracy continued to increase over the course of the epochs, while validation accuracy then decreased. The divergence of the two lines indicates that the model may be overfit. The other plot shows trianing loss is much less than validation loss. This means the network may be overfitting.

1. 
