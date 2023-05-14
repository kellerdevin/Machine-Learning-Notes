Generator generates data and discriminator attempts to determine whether the data is real or fake. If fake the discriminator tells the generator why it believes the data is fake which helps the generator learn.

This process can be thought of as a two-player game where the generator is trying to fool the discriminator, and the discriminator is trying to correctly classify the inputs as real (from the training set) or fake (created by the generator).

The generator is trained to maximize the probability of the discriminator making a mistake, while the discriminator is trained to better distinguish real data from fake. This is done through a process of [[Backpropagation]] and [[Stochastic Gradient Descent]], similar to how other [[Neural Network]] are trained.

Loss
- The discriminator's loss is typically a binary cross-entropy loss. For a given batch of real and fake data, it computes the average negative log-probability that the discriminator correctly classifies the data.
- The generator's loss is also a binary cross-entropy loss, but it is computed differently. Instead of trying to correctly classify the data, the generator tries to maximize the probability that the discriminator incorrectly classifies its outputs as real.
- Model uses [[Binary Cross Entropy]] for this
- For the discriminator, the loss will be high if it assigns high probability to fake images being real (i.e., it gets fooled by the generator), or real images being fake.
- For the generator, the loss will be high if the discriminator correctly identifies its generated images as fake. The generator's goal is to minimize this loss, i.e., to fool the discriminator as much as possible.

Mode Collapse
- This occurs when the generator produces very similar outputs for different inputs. Ideally, the generator should produce diverse outputs, but in mode collapse, the generator finds a few examples that can fool the discriminator and just keeps producing variations of those. This leads to a lack of diversity in the generated data.
- Techniques to mitigate model collapse:
	- **Minibatch discrimination**: This is a technique where the discriminator is allowed to look at multiple examples in combination, rather than in isolation. This can help it detect if the generator is just producing the same output over and over again.
	- **Feature matching**: This technique involves changing the objective function that the generator is trained with. Instead of trying to directly fool the discriminator, the generator is trained to make the features of the generated data match the real data. This can help to ensure that the generator produces diverse outputs.

GAN variants
- **DCGAN (Deep Convolutional GAN)**: This is a type of GAN that uses convolutional layers in the generator and discriminator. This architecture is especially useful for tasks related to images. The use of convolutional layers allows the model to take advantage of the 2D structure of images.
- **WGAN (Wasserstein GAN)**: This variant of GAN introduces a new loss function called the Wasserstein loss. The idea is to measure the distance between the real and generated data distributions in a more meaningful way. WGANs tend to be more stable during training and less prone to mode collapse compared to standard GANs.
- **CGAN (Conditional GAN)**: This type of GAN includes additional information (apart from the noise vector) as input to the generator and the discriminator. For example, if you're generating images of digits, you might include the digit class (0 through 9) as an additional input. This way, you can generate data from a specific class by conditioning the GAN on that class label.

Common Applications of GANs
- Image Synthesis: This is perhaps the most famous application of GANs. They can be trained to generate new images that resemble a given dataset. For example, GANs have been used to generate realistic human faces, create artwork, and even design clothing.
- Image-to-Image Translation: GANs can be used to translate one type of image into another. For example, you could use a GAN to turn a black and white photo into color, or to transform a daytime scene into a nighttime scene. This is done by training the GAN on pairs of corresponding images from the two domains.
- Super-Resolution: GANs can be used to increase the resolution of images. This is done by training a GAN on pairs of low-resolution and high-resolution images. The GAN learns to map from the low-resolution input to a high-resolution output.
- Anomaly Detection: GANs can also be used in anomaly detection, where the task is to identify unusual data. This can be done by training a GAN on the normal data, and then using the discriminator to score new data. Data that the discriminator thinks is 'fake' can be considered an anomaly.
- Data Augmentation: GANs can be used to generate additional training data. This can be useful when you have a small amount of labeled data and a lot of unlabeled data. You can train a GAN on the unlabeled data to generate more examples for your training set.

[[Semi Supervised Generative Models]]

[[Generative Models]]
