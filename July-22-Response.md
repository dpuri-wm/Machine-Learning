1. When a categorical column is split into new columns with values being stored as either 0 or 1, this is called a one-hot-encoded column. The source values are discrete, because the value can only take on 2 numbers: 0 or 1. Ex: [0,1,0] refers to second class, under the class feature.

2. Dense features specify the presence and absence of data (usually by a zero). They can be useful because the model will work properly even with missing information. For example, in DATA 141, missing values were indicated as NaN. However, the model may not eba ble to interpret this string and would lose functionality. 

3.  ![Screen Shot 2020-07-25 at 4 50 17 PM](https://user-images.githubusercontent.com/60228374/88466101-05bedf00-ce97-11ea-8f97-37a87d306771.png)

    ![Screen Shot 2020-07-25 at 4 50 26 PM](https://user-images.githubusercontent.com/60228374/88466114-20915380-ce97-11ea-9de6-b5a8072165c0.png)

    ![Screen Shot 2020-07-25 at 4 53 37 PM](https://user-images.githubusercontent.com/60228374/88466151-75cd6500-ce97-11ea-84f5-c470449ff067.png)
    
    ![Screen Shot 2020-07-25 at 4 53 47 PM](https://user-images.githubusercontent.com/60228374/88466161-8b428f00-ce97-11ea-8a98-4c7268f2649f.png)

    From the ROC curve, its clear to see that the rate of true positives is increasing much faster than false positives, in the beginning of the graph. However, the curve levels off. It reveals overfitting. Both probability models are pretty spread out, with a slight skew to the right. The boosted trees classifier shows a distirbution with 2 peaks, most likely indicating that it is the better classifier. 
    
    
1. ![Screen Shot 2020-07-25 at 4 58 45 PM](https://user-images.githubusercontent.com/60228374/88466235-30f5fe00-ce98-11ea-9a6d-8b05f77540eb.png)

    
