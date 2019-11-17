

### Definitions:

**Convolution**

It is a process of combining two functions to produce a third function. In the case of CNN, it is executed by sliding the kernel  over the input (image) and getting an output. It keeps the spatial relationship between pixels.


**Filters/Kernels**

Kernels are matrices which slides through the input (image) during the convulution process. It helps to extract features out of the input. Depending upon the values of the kernel matrix, we produce different feature maps. Applying kernel produces a scalar output.


**Epochs**

An Epoch occurs when a full set of training data is passed and backpropagated through the neural network.

**1x1 Convolution**

It's a convolution filter of size 1x1. The size of the input (image) remains unchanged. It keeps a very detailed information(at pixel level) of the image.

**3x3 Convolution**

It's a convolution filter of size 3x3. This matrix is used very widely.

**Feature Maps**

A feature map is the result of the convolution process. When a kernel slides through the input (image) and executes the convolution process, the output is a feature map.
                                                                                                                                                  

**Activation Function**

The output of the convolution process is linear, so Activation function is used to add non-linearity in the model. It gives the neural network the ability to learn complex data such as audio, video etc.

**Receptive Field**

It is about how much information a pixel holds at a convolution layer of the other predecessor layers.
The receptive field of the last layer must be atleast the size of the object we are looking at.
