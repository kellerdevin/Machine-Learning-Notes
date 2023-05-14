RNN stands for Recurrent Neural Network, which is a type of neural network used for processing sequence data such as time series, natural language processing, and speech recognition.

In an RNN, the output of a previous time step is fed back to the network as an input to the current time step. This allows the network to retain information from previous time steps and use it to make predictions or decisions in the current time step.

In contrast to feedforward neural networks, which process an input in one direction from input to output, RNNs have loops in them, allowing information to persist across time. At each time step, the RNN takes an input vector and produces an output vector, which is then fed back into the network at the next time step along with the new input vector.

The key feature of RNNs is that they maintain a hidden state that captures information from previous time steps, which is then used to influence the output at the current time step. This allows the network to model the temporal dependencies between inputs and outputs in sequence data.

The most common type of RNN is the [[Long Short-Term Memory Networks]] (LSTM), which is designed to overcome the problem of vanishing gradients that can occur in regular RNNs due to the repeated multiplication of gradient values. LSTMs use a series of gates to control the flow of information through the network, allowing them to selectively remember or forget information from previous time steps.

RNNs use the same set of weights and biases across all time steps to process sequential data. This means that the same weights and biases are applied to each input in the sequence. The output of the previous time step is fed back into the network along with the current input, allowing the network to take into account information from previous time steps.

Vulnerabilities of RNN
[[Vanishing Gradient Problem]] occur in RNNs when the gradients become too small and the weights are updated at a very slow rate. This problem occurs because the gradients are multiplied by the same weights at each time step, causing the gradients to either explode or vanish over time.

Optimization Algorithms
[[Attention]]