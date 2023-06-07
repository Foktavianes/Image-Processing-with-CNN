# Image-Processing-with-CNN
The .ipynb contains image processing for CIFAR10 datasets which contains 4 dimension data.
I am implemented pre-trained model to train the model with pre-trained model, such ResNet50, VGG16,DenseNet121, EfficientNetB0, NASNetMobile.

The .ipynb contains loss and accuracy for train and test set and which model is better suited to handle the CIFAR10 datasets

Brief explanation on each model architecture:
1. ResNet 50: (50 convolutional layers)

stage 1: Initial processing on the input image
stage 2 - 5: residual blocks with increasing number of filters in each block compared to previous stage. features obtained from prev stage are gloablly averaged, reducing dimension to 1x1 feature. generate final classification scores and softmax to produce prob. 

2. VGG16:

13 convolutional layers where each layer followed by a ReLU. The pooling layers progressively reduce the spatial dimensions of the feature maps. VGG16 has three fully connected layers towards the end of the architecture. then, softmax.

3. DenseNet121:

4 dense blocks. dense block performs a series of operations, typically involving batch normalization, a rectified linear unit (ReLU) activation function, and a 3x3 convolution. Transition block typically consists of batch normalization, a 1x1 convolution for dimensionality reduction, and an average pooling layer with a 2x2 window and a stride of 2.

4. EfficientNetB0:

series of convolutional layers, referred to as the stem layers, which extract basic features from the input image.
Multiple Blocks: EfficientNetB0 consists of multiple blocks, with each block composed of repeated layers.
Squeeze-and-Excitation (SE) Blocks: EfficientNetB0 incorporates SE blocks to recalibrate the importance of different channels in the feature maps.

5. NASNetMobile:

Stem Convolutional Layers: NASNetMobile begins with a series of convolutional layers, referred to as the stem layers, which extract basic features from the input image.
Cell Architecture: The core building block of NASNetMobile is the "cell." The cell architecture is composed of multiple "normal" and "reduction" cells stacked together.
Normal Cells: Normal cells capture complex patterns and feature interactions within the network.
Each normal cell consists of multiple connected nodes, each representing an operation, such as convolution or pooling.
Reduction cells typically include operations like pooling or strided convolutions to downsample the feature maps.
