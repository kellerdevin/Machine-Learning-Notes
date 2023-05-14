Max pooling is a technique used in [[Convolutional Nerual Network]](CNNs) to reduce the size of feature maps while preserving the most important information.

In max pooling, the input feature map is divided into a set of non-overlapping rectangular regions, called pooling windows. For each pooling window, the maximum value within the window is taken and used as the output for that region. This output value represents the presence of a certain feature in that region, regardless of its exact position.

The main advantage of max pooling is that it reduces the spatial dimensions of the feature maps while keeping the most important features. This makes the network more efficient by reducing the number of parameters it needs to learn, and it also helps to prevent overfitting by removing irrelevant details.

For example, in image recognition, max pooling can be used to detect important features such as edges, corners, and textures. By reducing the resolution of the feature maps, it helps the network to focus on the most important features and improve its accuracy in classifying images.

Hyper Parameters
The **filter size** refers to the dimensions of the pooling window that slides over the feature map. For example, a common filter size is 2x2, which means that the max pooling operation is applied over non-overlapping 2x2 regions of the feature map.

The **stride** is the distance that the pooling window moves across the feature map at each step. For instance, a stride of 2 means that the pooling window skips every other column and row of the feature map, resulting in a downscaled feature map that is half the size of the original.

**Benefits of Max Pooling**
-  It reduces the number of parameters in the model, which can help to avoid overfitting and reduce computational complexity.
- It provides a degree of translational invariance, which means that the network can still recognize the same features even if they appear in different locations within the input image.
- It helps to preserve the most salient features in the feature maps, which can improve the robustness and generalization of the network.

**Limitations of Max Pooling**
- It can lead to information loss, because it discards all the other values within each window except for the maximum value. This can potentially cause problems if the max value is not representative of the underlying features within that window.
- Max pooling can be sensitive to small translations or rotations in the input image, because it is only looking for the maximum value within each pooling window. This can make the network less robust to variations in the input.