# Indoor-Scene-Recognition

## Aim 
This project aims at building Deep learning system to recognise indoor scenes using R programming. Indoor scene recognition is a challenging problem since some indoor scenes can be well defined by global spatial and structural properties, while others are better characterized by the objects included in the space. The task is to build a predictive model to predict the type of indoor scene from the image data.

## Data set
The dataset is a subset of a larger dataset for indoor scene recognition. 

More information is available here: http://web.mit.edu/torralba/www/indoor.html.

The images are divided into train, validation, and test folders, each containing the folders related to the type of the room in the image (i.e. the categories of the target variable): bathroom, bedroom, children_room, closet, corridor, dining_room, garage, kitchen, living_room, stairs. The number of images available for each scene is variable and it ranges from 52 to 367 in the training set, with validation and test sets being roughly half the size.

The images taken are in numerical RGB tensors of width/height of 64 × 64.

## Convolutional Neural Network

To build a Convolutional neural network, we require configuring the layers of the model as follows:

**1.Convolution Layer:** A convolution layer extracts features from an image or a part of an image. We are specifying three parameters here: + Filters -- This is the number of filters that will be used in the convolution. E.g 64. + Kernel size -- The length of the convolution window. E.g. (3,3) or (5,5). + Activation -- This refers to the function of the regularizer. For example, ReLU, Leaky ReLU, Tanh, and Sigmoid.We shall stick to ReLU for our model.

**2.Pooling Layer:** This layer is used to reduce the size of an image.We shall use a constant pool size of (2,2).

**3.Flatten Layer:** This layer reduces an n-dimensional array to a single dimension.

**4.Dense Layer:** This layer is fully connected, which means that all of the neurons in the present layer are linked to the next layer. For our model, we have 128 neurons in the first dense layer and 10 neurons in the second dense layer.

**5.Dropout Layer:** To prevent the model from overfitting, this layer ignores a set of neurons (randomly).

## Model

I have designed 6 models characterized by different configurations to study and analyse the dataset. I will use data augmentation to generate additional training data from the available training samples, by augmenting the samples using a number of random transformations that provide realistic-looking images to expose the model to more aspects of the data and help it generalise better.  

I have used the below models for my project:

**1.Model 1:** Deep neural network

**2.Model 2:** CNN Model with 2 convolutional layers

**3.Model 3:** CNN Model with 3 convolution layers

**4.Model 4:** CNN Model with 3 convolution layers with data augmentation

**5.Model 5:** 2 Convolution layers with Batch normalization

**6.Model 6:** 2 Convolution layers and 2 dense layers with data augmentation
