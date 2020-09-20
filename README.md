# cifar10-with-deeplearning-architecture

About Dataset:
The CIFAR-10 and CIFAR-100 are labeled subsets of the 80 million tiny images dataset. They were collected by Alex Krizhevsky, Vinod Nair, and Geoffrey Hinton. 
The CIFAR-10 dataset consists of 60000 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images.

The dataset is divided into five training batches and one test batch, each with 10000 images. The test batch contains exactly 1000 randomly-selected images from each class. The training batches contain the remaining images in random order, but some training batches may contain more images from one class than another. Between them, the training batches contain exactly 5000 images from each class. 
classes are :1)airplane 2)automobile 3)bird 4)cat 5)deer 6)dog 7)frog 8)horse 9)ship 10)truck.

for this classification problem i used 2 architecture.first i used MLP(Multilayer perceptron) and then i used CNN(Convolutional Neural Network) and last i used Transfer Learning with VGG16 for feature extraction.

MLP:
In mlp i used 11 fully layer with diffirent units.in all layer except the output layer i used relu activation function and in the output layer used softmax activatoin function.in this model i used dropout for reduce overfitting and i got 54.39% accuracy.

CNN:
In cnn i used 6 convolutional block and 4 maxpool block and then 2 fully layer and finally i used again softmax function.bottom i wrote the order.
(conv -> maxpool -> conv -> conv -> maxpool -> conv -> maxpool -> conv -> conv -> maxpool -> dense -> dense -> softmax)
for convolutional block i used diffirent number of filters and for pooling i used maxpooling.for reducing overfitting i used dropout and kernel regularization(L2) and in 100 epochs with 128 batch size,i got avrage 77% accuracy and the best accuracy i got 78%.

in both models we have overfitting.

Trasfer Learning:
In transfer learning i used Vgg16 for feature extraction and i deleted dense layers and after that i used 2 fully layers with diffirent units with relu functions and for output used softmax with 10 classes.
