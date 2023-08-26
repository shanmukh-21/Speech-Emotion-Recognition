# Speech-Emotion-Recognition

Speech Emotion Recognition is a challengeable task to improve human-computer interaction. In the given paper they introduced the model called "HDFDM" model i.e., Hybrid Deep Learning with Multi-type features Model. Implemented three layers CNN, DNN and LSTM
CNN (Convolution Layer):
    Convolution2D Layer with kernel-size = 3*3, stride-size = 2*2, activation function = 'relu'
    Maxpooling2D layer with pool-size = 2*2 and stride-size= 1*1
    Dropout layer with 50% neurons are being dropped
    Flatten layer to convert it into 1D vector
DNN (Deep Neural Network):
    Dense layer which helps in connecting each and every neuron connecting to the preceding layer.
    BatchNormalization Layer is done to to reduce the range of the values
    Dropout Layer
LSTM (Long-short Term Memory):
    Bidirectional-LSTM layer is used for the weight updates of each and every neuron with the hidden units 512, 256 units
    Flatten layer

In order to view what are the layers are included, shape and paramter count use the summary() method to the used model.

I have used the EarlyStopping method since the size of the dataset is too large and the run time of an epoch is nearly taking 20 minutes and the use of EarlyStopping is it will check for the certain mentioned value of epochs if it doesnt changed from the before value either you can be controlled via loss or gain and use the parameter called verbose=1 it will help you to display the message whenever it is increased or decreased.

Compile the model and train the model i have considered loss function as CategoricalCrossEntropy since it is a multi-class classification and optimizer as adam.

With the help of matplot lib library i have plot the graph between accuracy as well as loss with epoch to check whether the condition is overfitting or underfitting. 
    
Download the dataset of Emodb Audio Files from here:
    [https://www.kaggle.com/datasets/piyushagni5/berlin-database-of-emotional-speech-emodb]()
