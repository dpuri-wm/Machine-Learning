# CNNs and their Role in Medical Image Classification

 I'm thrilled to discuss my final project, Convolutional Neural Networks and their Role in Medical Image Classification. Utilizing all the knowledge I have learned in the summer data science classes, especially DATA 310, and seeing the results in my project was super gratifying! Additionally, I was able to create a project that combined my two interests: medicine and machine learning. As a pre medical student with a strong interest in data science, this project showed me just how relevant technology and artificial intelligence is in the healthcare industry. It is quite literally our future, and I was able to see a little glimpse into how artifical intelligence may "take over" the role of a radiologist in diagnosing illnesses.
 
 The goal of my CNN model I created was to do a binary classification of chest X-ray exams, classifying between healthy (0) exams, and cardiomegaly present(1). After my research of misdiagnosis in the United States (discussed more in my problem statement), I was shocked that more emphasis was not being placed on women's heart health. The University of Leeds in the UK found that women are 50% more likely to receive the wrong diagnosis after having a heart attack compared to men, as women's pain is often overlooked. One reasons is because women's symtpoms of a heart attack present differently than they do in men. Women often complain of indigestion, and thus, a chest X-ray is not examined. However, in many cases, if a chest X-ray were taken, doctors may diagnose cardiomegaly - an enlarged heart condition that does not pump blood effectively. Thus, hoping to improve research of and diagnosis of cardiomegaly, I created a CNN to diagnose it. 
 
 My data was obtained from the U.S. National Library of Health's open access biomedical image collection. I downloaded 120, 200 x 150 pixel images of chest X-ray scans. This is obviously a very small dataset. I would have loved to include a much larger dataset, but due to the processing capabailities of my 2012 macbook air, I have to work within the limitations. I set up a train/test file structure and assigned 90 images to train and 30 images to test, with each having a 1:1 ratio of normal/cardiomegaly chest X-ray scans. I was able to flow these images into pycharms. In general, my images had high resolution. They also had whitepsace on the sides.
 
 Next, it was time to create my model. I displayed the architecture and the model itself on my poster. My CNN had 3 convolutional layers with an increasing number of filters in each layer (16,32,64) to pick up on the finer features of these scans. I included a MaxPooling2D layer after each layer to reduce dimensionality and down sample. I also included the signmoid function to get classification predictions in the last neuron layer. When compiling the model, I used binary_crossentropy as the loss function since my problem is a binary classification issue. It will compute the cross entropy loss between true labels and predicted labels. Since I'm working with categorical data as opposed to continuous data, accuracy is a good metric and loss is a good measure of the error.
 
 Overall, I would say my model performed pretty well. I received a training accuracy of .8333 and test accuracy of .8000. My training accuracy increased over the period of all the training epochs. When I tried training the data on the validation data as well, overfitness was experienced. I played around by adding more layers, but ultimately, there is a balance between overfitting and accuracy that was reached. I played around with the model and fed images into it to see what the model would classify the image as, and it did well!
 
 After fininshing my project, I found similar research online conducted by Anoop Singh, a machine learning engineer. He created a CNN to also detect cardiomegaly. Although our CNN architecture was similar, his included kernel_size, padding, and Global Average Pooling layers to control overfitting. His dataset was also quite large, with about 100,000 X-ray scans total. Because he had included more normal scans, his CNN had a bias towards "No Findings". He reached an accuracy of .95. 
 
 I'm convinvced that with more experimentation I could also reach .95! To accomplish this, I would first need to to increase the dataset size. This can be done with a better laptop. Additionally, I want to utilize image augmentation including horizontal flips and random crop/zoom. This could also increase the dataset size. I want to add more convolutional layers, and even test the model with images outside the dataset I curated. The possibilites are endless. Future extensions of my project could involve classifying the severity of cardiomegaly (mild, severe, etc.). Moreover, I did a little research on how radiolgoists actually diagnose cardiomegaly - through something called the cardiothoracic ratio. I could implement this to "count" pixels, with a little more knowledge in segmentation or object detection. 
 
 Overall, this project was really fun to make! My final project also illustrates the enormous potential artifical intelligence has in the healthcare industry in general. Machine learning engineers have already developed models to detect brain cancer, arrythmias, Alzheimer's, diabetes, and other illnesses. The list goes on and on. Aside from classification, CNNs could be used to predict continuous data types - like blood cell count, and whatnot! AI could reduce the time patients await their biopsy results, as oftentimes, part of the delay is attributed to the pathologist requiring a second opinion. These convolutional neural networks could work like a second set of eyes when diagnosing.
 
 It's apparent from my research that convolutional neural networks can help remedy the issue of misdiagnosis in the United States. 
 
 