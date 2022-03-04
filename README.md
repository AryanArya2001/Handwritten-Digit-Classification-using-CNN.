Handwritten Digit Classification using CNN

In this project i demonstrated how to create and train a simple Convolutional Neural Network(CNN) for classifying handwritten digits from a popular dataset known as MNIST dataset.MNIST dataset is a dataset of 60,000 small square 28×28 pixel grayscale images of handwritten single digits between 0 and 9.


Major Steps used to Create this Model are

1)Loadig the Dataset :As mentioned dataset used in this model is MNIST.After loading necessary libraries required for this model,load the MNIST dataset using :

(X_train, y_train) , (X_test, y_test) = keras.datasets.mnist.load_data()

To load the dataset in the model,and dividing it into two sets which are known as Training set and Testing set.

2)Process the Dataset: Now Data has to be processed, cleaned, rectified in order to improve its quality. CNN will learn best from a dataset that does not contain any null values, has all numeric data, and is scaled. So, here we will perform some steps to ensure that our dataset is perfectly suitable for a CNN model to learn from. From here onwards till we create CNN model, we will work only on the training dataset. 

3)Create and train a CNN:Now aftter processing the dataset create a CNN model using Tensorflow library.In the CNN model created, there is an input layer followed by two hidden layers and finally an output layer. In the most simpler terms, activation functions are responsible for making decisions of whether or not to move forward.

Once the model has been created, it is time to compile it and fit the model. During the process of fitting, the model will go through the dataset and understand the relations. It will learn throughout the process as many times as has been defined. In our example, we have defined 10 epochs. During the process, the CNN model will learn and also make mistakes. For every mistake (i.e., wrong predictions) the model makes, there is a penalty and that is represented in the loss value for each epoch (see GIF below). In short, the model should generate as little loss and as high accuracy as possible at the end of the last epoch.

4)Make Prediction: To evaluate the CNN model so created you can run:

y_predicted_by_model = convolutional_neural_network.predict(X_test)

The above code will use the convolutional_neural_network model to make predictions for the test dataset and store it in the y_predicted_by_model dataframe. For each of the 10 possible digits, a probability score will be calculated. The class with the highest probability score is the prediction made by the model. For example, if you want to see what is the digit in the first row of the test set



