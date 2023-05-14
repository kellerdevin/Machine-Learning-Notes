
ResNet (short for Residual Network) is a specific type of [[Neural Network]]  architecture that was developed to address the [[Vanishing Gradient Problem]]

In ResNet, the solution to the vanishing gradient problem is to introduce skip connections, which allow information to flow directly from earlier layers to later layers.

Skip connections allow the input of a layer to be added to the output of a later layer, so that the output of the earlier layer can directly influence the output of the later layer. This means that the gradients flowing through the network during [[Backpropagation]] have a more direct path to earlier layers, which helps to mitigate the vanishing gradient problem.

Now, in addition to the skip connections, ResNet also uses residual connections, which are essentially the same thing as skip connections, but with a slight modification. Instead of simply adding the input to the output, the residual connection adds the input to the output after applying a transformation. This transformation is implemented using a series of convolutional layers and batch normalization layers.

The idea behind the residual connection is to allow the network to learn residual functions, which can more easily capture the difference between the input and the desired output. This helps the network to learn more effectively and can improve its performance.

ResNet is a neural network architecture that uses skip connections and residual connections to address the problem of vanishing gradients. The skip connections allow information to flow directly from earlier layers to later layers, while the residual connections allow the network to learn residual functions that capture the difference between the input and the desired output.


