# Image-Classification-Model-development
#Model architecture:
This algorithm classifies images between multiple groups of classes. In this algorithm used convolutional layers and max pooling layes.
The output layer we are using is a Dense layer with softmax activation. The number of nodes in the output Dense layer is equal to the number of classes in the training dataset. The softmax activation assigs a prediction number to each node, these prediciton numbers add up to 1 and can considered as probabilities assigned to each output class. The model makes it's prediction based on the highest probability values. 
