# Deep-Learning-Model
Different practices using Deep learning Structure
# Deep Learning Model Practice: Music genre classification
## CNN Model: train a CNN based classifier on the Mel spectrograms to predict the corresponding music genres
 First parallel branch:
  1. one convolutional layer processing the input data with 3 square filters of size 8, padding and leaky ReLU activation function with slope 0.3.
  2. one pooling layer which implements Max Pooling over the output of the convolutional layer, with pooling size 4.
  3. a layer flattening the output of the pooling.

- Second parallel branch:
  1. one convolutional layer processing the input data with 4 square filters of size 4, padding and leaky ReLU activation function with slope 0.3.
  2. one pooling layer which implements Max Pooling over the output of the convolutional layer, with size 2.
  3. a layer flattening the output of the pooling..

- Merging branch:
  1. a layer concatenating the outputs of the two parallel branches.
  2. a dense layer which performs the classification of the music genres using the approppriate activation function.
Optimise using a mini-batch stochastic gradient descent algorithm. Train for 50 epochs.
Plot the loss function and the accuracy versus the number of epochs for the train and validation sets. Aachieved over 70% accuracy on the validation set.
## CNN-RNN Model: CNN-RNN based classifier on the Mel spectrograms to predict the corresponding music genres
CNN-RNN architeture:
1. a convolutional layer with 8 square filters of size 4.
2. a max pooling layer that halves the dimensionality of the output.
3. a convolutional layer with 6 square filters of size 3.
4. a max pooling layer that halves the dimensionality of the output.
5. an LSTM layer with 128 units, returning the full sequence of hidden states as output.
6. an LSTM layer with 32 units, returning only the last hidden state as output.
7. a dense layer with 200 neurons and ReLU activation function.
8. a layer dropping out 20% of the neurons during training.
9. a dense layer which outputs the probabilities associated to each genre.

Optimise using a mini-batch stochastic gradient descent. Train for 50 epochs.
Plot the loss function and the accuracy on the train and validation sets over the epochs. Achieved over 50% accuracy on the validation set.
## VGG-CNN network:
Train for 50 epoches
Achieved over 85% accuracy.
