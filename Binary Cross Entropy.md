Binary Cross-Entropy loss is a loss function commonly used in machine learning models for binary classification problems, where the output of the model is a probability that the given input point belongs to a certain class.

The mathematical formula for Binary Cross-Entropy loss for a single data point is:

Loss = -[y * log(p) + (1 - y) * log(1 - p)]

Where:

-   y is the actual class label (0 or 1 in binary classification)
-   p is the predicted probability of the point belonging to class 1

Basically, what this loss function does is to compare the model's predicted probability distribution with the actual distribution. The 'log' function is used because it penalizes predictions that are confident and wrong.
