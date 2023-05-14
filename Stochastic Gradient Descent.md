**

Gradient descent  

-   gradient descent is like walking down a hill in the steepest direction until you reach the bottom, where the slope is zero. By doing so, the algorithm is able to find the optimal values of the model's parameters that minimize the loss function and improve the model's performance.
    
-   Momentum is a technique used in Stochastic Gradient Descent (SGD) where the optimizer accumulates the gradients from previous steps and uses them to adjust the current step, allowing for smoother updates and faster convergence to a minimum. The momentum term is typically introduced as a new parameter in the update rule that is proportional to the previous gradients.
    
-   Acceleration is a technique used in Stochastic Gradient Descent (SGD) that scales the momentum term by the current gradient, allowing the optimizer to accelerate or decelerate in response to the current gradient. This can help the optimizer converge more quickly to a minimum.

- Backpropagation: The key step in training a neural network with gradient descent is backpropagation. It involves computing the gradient of the loss function with respect to the parameters of the network. The gradient is calculated using the chain rule of calculus. Starting from the output layer, the gradient is propagated backward through the layers. For each layer, the gradients are computed with respect to the weights and biases, as well as the inputs of the layer. This process allows us to determine how changes in the weights and biases contribute to the overall error.
