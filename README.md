# Image-Classification-Model-development
This algorithm classifies images between multiple groups of classes.
## Model Architecture: 
The input to the network is an image of dimensions (150, 150, 3). The first two layers have 32 channels of a 5*5 filter size and the same padding. Then after a max pool layer of stride (2, 2) then Batch Normalization layer to maintain the mean output close to 0 and the output standard deviation close to 1. Then two layers have convolution layers of 64 filter size and filter size (3, 3). This is followed by a max-pooling layer of stride (2, 2) which is the same as the previous layer then Batch Normalization layer. Then there are 2 convolution layers of filter size (3, 3) and 128 filters. This is followed by a max-pooling layer of stride (2, 2) which is the same as the previous layer then Batch Normalization layer. We flatten this output to make it a (1, 25088) feature vector. After this there is 1 fully connected layer with 256 neurons, After that a dropout layer. The output layer we are using is a Dense layer with softmax activation. The number of nodes in the output Dense layer is equal to the number of classes in the training dataset. The softmax activation assigs a prediction number to each node, these prediciton numbers add up to 1 and can considered as probabilities assigned to each output class. The model makes it's prediction based on the highest probability values. All the hidden layers use ReLU as its activation function. ReLU is more computationally efficient because it results in faster learning. 
## Data reprocessing techniques:
Keras has a module with image-processing helping tools, located at keras.preprocessing.image. It contains the class ImageDataGenerator, which lets you quickly set up Python generators that can automatically turn image files on disk into batches of preprocessed tensors.
## Evaluation results:
We are using precision, recall, f1 score and acccuracy.
## Requirements

  Install the required python modules.

   ```
      pip install -r requirements.txt
   ```
## Observations for misclassifications:
For misclassification in the buildings list, we see that most of the predictions are of street becuase in the training images we can see that there are buildings present in the streets images. The same issue is for mountains and glaciers.
