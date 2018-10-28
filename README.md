# EC601_miniproject_2
This is the homework of miniproject 2

# Pretrained model
## Introduction
Using a pretrained model can be an easy, fast and effective way to images recognization. In this model we use a concept of transfer learning.
Transfer learning is a technique that shortcuts much of this by taking a piece of a model that has already been trained on a related task and reusing it in a new model. 

So with a given pretrained model, which has been trained by the images from images.net, we retrain the model and give out the correct answer of images classification. The time we use to retrain is shorter than train a new model relatively. And the accuracy is quite high, upto 80 to 90 percent.

## Inplementation of program
Put```retrain.py``` and ```test.py``` into your working directory. Then create a new folder named ```training_images``` and put your training dataset(images) into this folder. Under this folder you need to creat two folder with the class of images respectively. Next, you need to create a new folder in the working directory named```javascript test_images``` and put your test dataset (images) into this folder, images in this folder should contain images from both class, and should put them togather instead of seperating them as training set.

Then you can run the ```test.py``` first. After successfully running this program, you have finishing building the model. Next, you can test your model by running  ```test.py```, and the program will show you the tag of images in test set to validate this model, and you can see the result there.

P.S. You can test the program with the given dataset in the folder ```pretrained_dataset```


# CNN model
## Introduction
Using Convolutional Neural Network to build up a model from begining can be another way. The way we are going to achieve it is by training an artificial neural network on few thousand images and make the NN(Neural Network) learn to predict which class the image belongs to, next time it sees an image having the corresponding class tag in it. We use the keras model in Tensorflow to achieve it.
First we need to build up a layer with Conv2D to contain images, to implement convolution. Then we need to perform pooling operation on the resultant feature maps we get after the convolution operation is done on an image. Then we need to flatten the 2D-array in to one dimensional single vector. Following, we need to create a fully connected layer, and to this layer we are going to connect the set of nodes we got after the flattening step, these nodes will act as an input layer to these fully-connected layers. Finally we need to bulid an output layer with only one unit to indicate the class which the image belongs. 

After buliding the model, we need to compile it. To prevent overfitting, we also need to pre-process the image.

Then we will fit data into our model, since this model is new with no experience as the first model mentioned above, we need to iterate the training process for more than once. In this example, we take 25 as an example.

## Inplementation of program
Put ```cnn.py``` into your working directory, then create a folder named ```dataset``` to contain your dataset to train and test the model. Then you can go into the dataset folder, and create two folder named ```training_set``` and ```test_set``` to contain your training set and test set respectively. In both folder, you need to create different folder for images from each class, and tag their class as the name of folder.

Then you can run ```cnn.py``` to build and test the model. Since this is an brand new model with no experience, so it will take a very long time to train this model.

P.S. You can test the program with the given dataset in the folder ```cnn_dataset```

Dataset link
===================
pretrained model dataset: https://drive.google.com/file/d/1-ecrKbMvJeDC9lk9QqEZjIX5EO_MPVar/view?usp=sharing

cnn model dataset: https://drive.google.com/file/d/1hfysE__1bqxRAhPEs9WF8ZgRzq8G8JYx/view?usp=sharing
