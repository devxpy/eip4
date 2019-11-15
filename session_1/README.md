[Assignment result](Untitled.ipynb) - `[0.03444110200128452, 0.9901999831199646]`

## Convolution 

Convolution in mathematics is a simple matrix multiplication operation.

In image classificaion, a matrix multiplication allows us to selectively increase/decrease the significance a pixel has on the output.

These are also called as "weights", signifying the weightage a pixel has in the final output.

It's entriely possible to manually assign a weight to each and every pixel, (which is simply a real value between 0 and 1), but it's computationally faster to express this in terms of a matrix multiplication.

## Filters

Filters are simply the 2nd term, in the matrix multiplication between the pixel values of the input image, and the filter itself that produces a convolution.

## Epochs

This is the number of training cycles.

In image classsification, a training dataset consists of many images. After all the images in a training dataset are passed through the network, the total loss (which is a function of the distance of inferred labels from the ground truth),  is calculated, and the weights in the network are updated according to the backpropagation algorithm.

Often, a single epoch is not enough to get the best accuracy, so we have to train a network multiple times to get good accuracy.

## 1x1 Conv

Since a 1x1 matrix multiplication is the same a linearly multiplication of 2 numbers, in image classification, its the equivalent of multiplying all the pixel values of an input layer with a floating point value (call the weight).

## 3x3 Conv

In this operation we convolute, (or multiply) each 3x3 contiguous sub-matrix of an input matrix with another 3x3 matrix (the filter) to get an output layer in which each pixel is formed as a result of this matrix multiplication.

For each row in the input matrix of size N, written down as - <a1, b2, a3, ..., aN-2, aN-1 aN>, its easy to see that contiguous sub-matrixes of size 3 can be placed at  each of the <a1, a2, a3, ..., aN-2> th places of input matrix. 
So, the number of sub-matrices = (N-2) - (1) + 1 = N - 3 + 1 = N - 2.

Since each sub-matrix maps to a single pixel in the output layer, we get a nice little formula, that says we get exactly N-2xN-2 pixels in the output layer, after a 3x3 conv. is applied to an input of size NxN

## Activation Function

After applying the weights on each pixel value of the input image, its necessary to devise a way to accept or reject values. An activation function defines a cutoff value, below which we don't consider the pixel to have any effect on the output of the network.

This accept/reject function is necessary, simply because the output of a classifier is generally a binary value. Like is this an image of a cat or a dog?

A small implementation detail is that the activation function is generally defined as a continous value after the cutoff and not just an abrupt binary mapping, because it helps the gradient descent algorithm to function properly.

## Receptive Field

This is the raw number of pixels of original input image any given pixel of a layer inside the network casts a shadow on. 

This number is an important metric, because it very clearly defines the number of pixels from the input image, that can directly or indirectly affect the value of a single pixel in any layer.

This arises from the fact that in convolution, any given pixel (in the subsequent layers after the input layer) is the result of a matrix multiplication. 

When the same matrix multiplcation operation is applied multiple times, across multiple layers, the receptive field of a single pixel linearly increases with the number of layers.

