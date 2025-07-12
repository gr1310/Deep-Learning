# Generative AI course

**Deep Learning**

Input Layer --> Hidden Layers --> Output Layer
(Takes data)--> (processes data)--> gives output

While working with any kind of image, image consists of pixels.
Each pixel value belongs to [0-255] which is shade of that particular colour

Sequential model: When we want to create a simple sequential one-to-one model

FAPI model: when we want to create different architectures model

Flatten Layer: We cannot pass matrix data to the model, so we flatten it. Transforming 2D matrix into flattened layer (1D array). We give it the size of out input matrix

Dense: When we are using simple architecture of feed-forward network, when neurons are connected to next layer neurons. It is fully connected neural network.
Dense is hidden layer
We pass the number of neurons the layer should have
We also give activation function here

Dense layer is output layer too. Number of neurons in this layer should be same as number of outputs we want.

Activation Function: Allows us to add non linearity in the data.
In hidden layers, we generally use ReLu, because computations cannot be categorized.
For output layer, we use sigmoid if it's binary classification. But, for multilevel classification, we use softmax

![Sequential_model](image.png)

What is params?
The number of connections it is making along with the bias used. 784 x 5 + bias = 3920 + bias
For each neuron we add 1, so that makes it, 784 x 5 + 5 = 3925
Similarly, for output layer, 5 x 10 + 10 = 60

Total trainable parameters is the number of parameters we save for training purpose. Hence, 3925 + 60 = 3985

Compilation of model?

Optimizer: Loss for single values and how weights are optimized to reduce loss. eg. adam and gradient decent

Loss function: As we are working with categorical data we use categorical_crossentropy. Loss is the total loss after all iterations.

For evaluation of model we use metrics, eg. accuracy

Model.fit()?

We pass the data model is to be trained on, x and y train

Epochs: How many iterations are we gonna perform for the whole dataset.

Batch size: In a single collection or training instance, we'll consider 32 pieces at a time. We perform the optimization/backpropogation on these batches parallely

verbose: How much info we want to show

![Model train](image-1.png)
In every epouch how the 1875 number comes? It's total number of data / batch size
= 60000 / 32

We compare models based on loss, which has least loss is best.

Model.evaluate -> (loss, accuracy)

model.save('name.h5') -> this downloaded model can be used

To get the weights, model.get_weights()

_Architectures of Neural Network_

For simple basic feed forward neural network we use Sequential Model and a Dense Layer.

For complex NN,
