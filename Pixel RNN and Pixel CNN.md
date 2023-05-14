Pixel RNN and Pixel CNN are generative models that are used for image generation tasks. They are neural network models that can learn the probability distribution of the pixel values in an image and generate new images that are similar to the training data.

Pixel [[Recurrent Neural Networks]] (Recurrent Neural Network) is a type of generative model that works by modeling the probability distribution of the pixel values in an image one pixel at a time, from left to right and top to bottom. It does this by using a recurrent neural network to generate the pixel values one row at a time, conditioned on the previous rows. This allows the model to capture the dependencies between the pixels in the image.

Pixel [[Convolutional Nerual Network]] (Convolutional Neural Network) is another type of generative model that works by modeling the probability distribution of the pixel values in an image using convolutional neural networks. It does this by using a network of convolutional layers to generate the pixel values one pixel at a time, conditioned on the previous pixels. The model uses masked convolutions to ensure that each pixel is generated based only on the previously generated pixels.

Both Pixel RNN and Pixel CNN can generate high-quality images that are similar to the training data. They are able to capture the complex dependencies between the pixels in an image and generate new images that are highly realistic. However, they can be computationally expensive and may require a large amount of training data to achieve good performance.