# glalio-auth

# Project rock-scissors-paper

## Game description
There is a random agent who is the opponent of mine.It picks a picture from a pool of pictures and applies to it image processing techiques.Specifically, it applies ,firstly, vertical flip and after horizotal flip to the image to make it difficult to my agent to recognise the picture.The chance of application of both techniques are 50%.My agent is a machine learning model which has to recognise the image.If it succeeds it chooses the move which beats the one of the random agent and scores one point. If it fails to recognise the image it picks the wrong move.In this case if it's choice is the same as the random agent's move the score remains stable.On the other hand it loses one point.The total number of round is N.


## Data preprocessing
The data are about 2100 pictures 200p(height) x 300p(width) rgb. The first processing procedure is the transformation of them into grayscale pictures of 40p x 60p in order to train the models.After that the data gets normalized by dividing with 255 since it is the max value of the image pixels.It is used a train set and a a test set of splitting ratio 80/20.Then the models' training gets started.

In this project i used various models to evaluate their accuracies and scores. Firstly, i applied grid search for a svm with kernel='rbf' to find the best combination.Secondly, i also applied grid search for the random forest model in order to find the most effective.The same goes for the dense neural network model.The next is a convolution neural network.Lastly, grid search it is performed for a knn classifier.


## Results

The N = 100 rounds

### SVM classifier

Best Hyperparameters: {'C': 10, 'gamma': 0.1}

The score of agent is 71
Right recognitions are 77
Wrong recognitions are 23

### Random Forest classifier

Best Hyperparameters: {'max_depth': 20, 'min_samples_leaf': 1, 'min_samples_split': 2, 'n_estimators': 200}

The score of agent is 47
Right recognitions are 66
Wrong recognitions are 34

### Dense NN classifier

Best parameters found:  {'activation': 'relu', 'alpha': 0.0001, 'hidden_layer_sizes': (128, 64)}



### KNN classifier



### CNN classifier
