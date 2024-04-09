# Unc Landmark Classifier

This classifier trains a convolutional neural network to classify five of UNC's most famous campus landmarks: the Old Well, the Morehead-Patterson Bell Tower, Kenan Stadium, the Ackland Art Museum, and Wilson Library.

The images were taken straight from Google search engine results of the respective landmarks and were compiled into a total of over 2000 images across the five classes. The data was then cleaned up, removing any images that were not of a certain type (PNG, JPEG, JPG, or BMP) or images that were corrupted and had issues being uploaded. After the data cleanup, the data set was reduced to 1880 images in total. 

Each of the image's features was centered to be between [0,1] by dividing by 255. The images were split into training, validation, and test sets, and a neural network with five layers was trained on the images using 2D Convolutional Networks and ReLU activation function, before being extrapolated to the five classes with softmax activation. The model was trained across 20 epochs and was able to achieve a consistent 83 - 86% accuracy on the validation set by the final epoch across numerous trainings of the model.

The model was then used to predict members of the test set and achieved an 85% score, and a confusion matrix representing the data was plotted. In order to improve the model, I would suggest steps be taken to increase the amount of data used in training, find a suitable regularization for the model to prevent overfitting, and perhaps increase the complexity of the network or use other activation functions within the hidden layers to improve accuracy. Although my code includes an area to detect for a device GPU and regulates the usage of that GPU, there are known issues with attempting to use the GPU on an M1 MacBook Pro that as far as I can tell have not been resolved. 
