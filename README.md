# Convolutional Neural Networks for Sentence Classification

Train convolutional network for sentiment analysis. Based on "Convolutional Neural Networks for Sentence Classification" by Yoon Kim, [link](http://arxiv.org/pdf/1408.5882v2.pdf). Inspired by Denny Britz article "Implementing a CNN for Text Classification in TensorFlow", [link](http://www.wildml.com/2015/12/implementing-a-cnn-for-text-classification-in-tensorflow/).

We experimented this implementation for comparative study of sentiment analysis on Keras for Teano, Tesorflow, CNTK. 

CNN-non-static loss and accuracy: 
* In theano val_loss and val_acc in 1st epoch is 0.6931 and 0.5126 respectively. While in 10 epoch it is 0.3801 and 0.8708. 
* In Tensorflow val_loss and val_acc in 1st epoch is 0.6932 and 0.5000 respectively. While in 10 epoch it is 0.3434 and 0.8690.  
* In CNTK val_loss and val_acc in 1st epoch is 0.3691 and 0.5000 respectively. While in 10 epoch it is 0.2695 and 0.8690. 


## Some difference from original article:
* larger IMDB corpus, longer sentences; sentence length is very important, just like data size
* smaller embedding dimension, 20 instead of 300
* 2 filter sizes instead of original 3
* much fewer filters; experiments show that 3-10 is enough; original work uses 100
* random initialization is no worse than word2vec init on IMDB corpus
* sliding Max Pooling instead of original Global Pooling

## Dependencies

* The [Keras](http://keras.io/) Deep Learning library 

* The [Theano](http://deeplearning.net/software/theano/install.html#install) backend should be installed.

* The [Tensorflow](https://www.tensorflow.org/install/) backend should be installed. 

* The [CNTK](https://cntk.ai/pythondocs/setup.html) backend should be installed. 


