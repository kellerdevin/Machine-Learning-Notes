Maximum likelihood estimation (MLE) is a statistical method used to estimate the parameters of a probability distribution that best describe the observed data. 

In the context of generative models, MLE is used to estimate the parameters of the model's probability distribution that best describe the training data.

To illustrate this, let's say we have a dataset of handwritten digits (like the MNIST dataset) that we want to use to train a generative model that can generate new handwritten digits. We could represent each digit as a vector of pixel values, and model the probability distribution of these pixel values using a multivariate Gaussian distribution. The parameters of this distribution (the mean and covariance matrix) can then be estimated using MLE.

During training, the generative model learns to maximize the likelihood of generating the training data, given the estimated probability distribution. This is done by adjusting the model's parameters to minimize the negative log-likelihood of the training data.

Once the model is trained, it can generate new handwritten digits by sampling from the learned probability distribution. The generated digits will be similar in style and content to the training data, but not exact copies.