# glalio-auth

# Project rock-scissors-paper

## Game description
There is a random agent who is the opponent of mine.It picks a picture from a pool of pictures and applies to it image processing techiques.Specifically, it applies ,firstly, vertical flip and after horizotal flip to the image to make it difficult to my agent to recognise the picture.The chance of application of both techniques are 50%.My agent is a machine learning model which has to recognise the image.If it succeeds it chooses the move which beats the one of the random agent and scores one point. If it fails to recognise the image it picks the wrong move.In this case if it's choice is the same as the random agent's move the score remains stable.On the other hand it loses one point.


## Data preprocessing
The data are about 2100 pictures 200p(height) x 300p(width) Rgb. The fisrt processing procedure is the transformation of them into grayscale pictures of 40p x 60p in order to train the models.

In this project i used various models to evaluate their accuracies and scores. Firstly, i applied grid search for a svm with kernel='rbf' to find the best combination 

