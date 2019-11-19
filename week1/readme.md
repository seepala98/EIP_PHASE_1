# Assignment-1

## Seepala Venkata Sai Vardhan 

print(score) : [0.03320866822060198, 0.9919]

## Convolution

Convolution is basically a mathematical operation which consists of multiple element-wise matrix multiplication and addition.Convolution takes an input channel (an input image), convolves on top of a n x n kernel (typically 3 x 3 kernel) to give an output channel. Convolution is done to extract features out of an input channel through convolving with kernel.


Input channel of size 7 x 7 convolves on a kernel of size 3 x 3 to give output channel of size of 5 x 5

## Filters/Kernels

A filter or a kernel is an n x n matrix that extracts features from an input channel via convolution. It is a feature extractor. In Convolutional Neural Networks, the values inside the filter/kernel matrix are initially random. As the training process is carried out, the values inside the matrix change in accordance with the feature extracted by it.

Kernels in the initial layers extract basic features such as edges and gradients and as we dig deeper into CNN architecture, we observe that deeper layer kernels combine the information learned by previous layers to extract more complex features.

## Epochs

When a model is trained, it loops over the entire dataset several times, updating weights in the model after each image is encountered. One Epoch is defined as one forward and one backward pass over the entire dataset only once.

Dataset is usually divided into batches as it is computationally expensive to load the entire dataset onto the memory. Total no of training examples in a batch is known as batch size. No of passes (one batch at a time) required to complete one epoch.

If there are 1000 training examples, and batch size is 50, it takes 20 iterations to complete one epoch.

## 1x1 Convolution

When we write a deep convolutional neural network architecture, we often come across a situation where the number of parameters are too much to handle by GPU. So we reduce the kernel size. At this stage, if we use a 3 x 3 kernel, it is going to re-interpret the data and update the kernel weights accordingly.

To avoid this situation, we use a 1 x 1 kernel for convolution where it acts as a moderator that combines only those features which are semantically related. It acts as a channel reduction mechanism that also takes care of memory constrain on GPU.

## 3x3 Convolution

A 3 x 3 convolution involves a kernel of size 3 x 3 convolving over an input channel. Given an input channel of size m x n, if we convolve it over a 3 x 3 kernel, the kernel slides over the entire channel, convolving and results in an output channel of size (m-2) x (n-2).

The GPU computing libraries are usually built over 3 x 3 kernel size for optimization purpose. Higher kernel sizes (like 5 x 5 and 7 x 7) can be directly built from a 3 x 3 kernel. A 5 x 5 kernel can be built from two 3 x 3 kernels, 7 x 7 from three 3 x 3 kernels and so on.

## Feature Maps

The output of a convolution operation of a kernel over an input channel gives a feature map or an output channel. One kernel gives one feature map. Feature maps are also called as activation maps because, when a filter is applied, certain parts of an image are activated. A high activation means certain feature is found.

## Activation Function

An activation function basically maps input to a range of outputs. We take sum of products of input (from the previous layer) and their corresponding weights and apply activation function to it.

The activation function typically introduces non-linearity when it maps input to output. It decides which information should be filtered and which ones shouldn't. There are several activation functions such as ReLu, Sigmoid, Softmax, TanH etc.

## Receptive Field

Receptive field refers to the part of the image that is visible to one filter at a time. This is known as local receptive field. This receptive field increases as we stack more convolution layers. Ideally we want our model to look at the entire image in order to carry out analysis, in that case, global receptive field will be our image size.
