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

The score of agent is 54

Right recognitions are 67

Wrong recognitions are 33


![download](https://github.com/glalio/glalio-auth/assets/157219205/4b99cc39-d44d-4b64-b10d-797be32494d5)

### Random Forest classifier


Best Hyperparameters: {'max_depth': 20, 'min_samples_leaf': 1, 'min_samples_split': 2, 'n_estimators': 200}

The score of agent is 56

Right recognitions are 68

Wrong recognitions are 32


![download](https://github.com/glalio/glalio-auth/assets/157219205/ab6da887-88ff-4a5b-af76-9cf6078c268e)


### Dense NN classifier

Best parameters found:  {'batch_size': 64, 'epochs': 100}
Dense(128, activation='relu'),
Dense(64, activation='relu'),
Dense(3, activation='softmax')

The score of agent is -9

Right recognitions are 28

Wrong recognitions are 72


![download](https://github.com/glalio/glalio-auth/assets/157219205/fe844ec6-14c4-4772-b6dd-2293d36d7d7e)



### KNN classifier

Best parameters found: {'n_neighbors': 10, 'weights': 'distance', 'p': 2}

The score of agent is 48

Right recognitions are 61

Wrong recognitions are 39


![download](https://github.com/glalio/glalio-auth/assets/157219205/5f0c95c8-fa40-4478-a72e-ce939695fb55)



### CNN classifier

The score of agent is 7

Right recognitions are 37

Wrong recognitions are 63


![download](https://github.com/glalio/glalio-auth/assets/157219205/5938be35-6ff7-4b5f-b7f4-e3398aaeb048)
