# glalio-auth

#Project rock-scissors-paper

##Game description
There is a random agent who is opponent to mine.It picks a picture from a pool of pictures and applies to it image processing techiques.Specifically, it applies ,firstly, vertical flip and after horizotal flip to the image to make it difficult to my agent to recognise the picture.The chance of application of both techniques are 50%.My agent is a machine learning model which has to recognise the image.If it succeeds it choose the move which beats the choice of the random agent. If it fails to recognise the image 


##Data preprocessing
The data are about 2100 pictures 200p(height) x 300p(width) Rgb. The fisrt processing procedure is the transformation of them into grayscale pictures of 40p x 60p in order to train the models.

In this project i used various models to evaluate their accuracies and scores. Firstly, i applied grid search for a svm with kernel='rbf' to find the best combination 

