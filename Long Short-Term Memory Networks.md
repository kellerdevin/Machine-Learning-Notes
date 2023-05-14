The most common type of [[Recurrent Neural Networks]] is the long short-term memory (LSTM) network, which is designed to overcome the [[Vanishing Gradient Problem]] that can occur in regular RNNs due to the repeated multiplication of gradient values. LSTMs use a series of gates to control the flow of information through the network, allowing them to selectively remember or forget information from previous time steps.

LSTM stands for Long Short-Term Memory, which is a type of [[Neural Network]] architecture used for processing sequential data, such as text, speech, and time series data.

LSTMs have a unique architecture that includes a memory cell, input gate, output gate, and forget gate, which allows them to selectively retain and forget information from previous time steps. By selectively retaining and forgetting information, LSTMs can better maintain long-term dependencies in the data, and thus, they have become a popular choice for modeling sequential data.

LSTM has a unique cell state that can selectively retain or forget information based on the input data. This cell state is protected by gates, which are controlled by sigmoid activation functions, allowing the network to decide when to keep or forget information.

There are three main gates in an LSTM: the input gate, the forget gate, and the output gate. The input gate determines which information should be updated and added to the cell state. The forget gate decides which information to remove from the cell state. The output gate determines what information should be output from the cell state to the next stage of the network.

The LSTM architecture is particularly useful in tasks that involve long-term dependencies, such as language modeling, speech recognition, and stock price prediction, among others.

Describe the structure and function of the three gates in an LSTM?

**input gate**: controls how much new information is added to the memory cell. It takes in the current input and the output from the previous time step, and decides which parts of the new input to keep and which parts to discard. The gate does this by passing the input through a sigmoid activation function, which squashes the values between 0 and 1. A value of 0 means that the gate should discard that piece of information, while a value of 1 means that the gate should keep it.

The forget gate controls how much information from the previous time step is kept in the memory cell. It takes in the output from the previous time step and the current input, and decides which parts of the previous memory cell state to keep and which parts to discard. The gate does this by passing the output and input through a sigmoid activation function, similar to the input gate.

The output gate controls how much information from the memory cell is outputted to the next time step. It takes in the current input and the output from the previous time step, and decides which parts of the memory cell state to output. The gate does this by passing the output from the previous time step and the current input through a sigmoid activation function and then through a tanh activation function. The sigmoid function determines which parts of the memory cell state to output, and the tanh function scales the values of the output.

The memory cell is the "memory" of the LSTM. It stores information over time by selectively adding or removing information through the input and forget gates. The cell state is updated by adding the new input to the current memory cell state multiplied by the input gate, and subtracting the previous memory cell state multiplied by the forget gate. The updated memory cell state is then outputted through the output gate.

Use Cases:
Forecasting
[[Natural Language Processing]]
- Language modeling
	- LSTMs can be trained to predict the probability of the next word in a sentence, given the previous words. This is useful for tasks such as text generation, machine translation, and speech recognition.
- Sentiment Analysis
	- LSTMs can be used to classify the sentiment of a piece of text (e.g., positive or negative). This is useful for tasks such as analyzing customer feedback or monitoring social media.
- Text Summaries
	- LSTMs can be used to generate a summary of a longer piece of text, such as a news article or research paper. This is useful for tasks such as information extraction and content curation.


Optimization Algorithms:
[[Attention]]
