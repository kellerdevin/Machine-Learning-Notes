A Transformer is a type of [[Neural Network]] architecture that is commonly used for natural language processing tasks. Unlike traditional recurrent neural networks, Transformers do not require a sequential processing of input data, which makest hem more efficient for processing longer sequences of data.

Attention:
- The self-[[Attention]] mechanism is a key component of Transformers. It allows the model to focus on different parts of the input sequence when making predictions. In simple terms, self-attention measures the similarity between different words in a sentence to determine how much weight to assign to each word when generating output.
- Once the attention weights are computed, they are used to compute a weighted sum of the input sequence, where each element is weighted according to its attention weight. This results in a new representation of the input sequence that selectively focuses on the most relevant parts of the sequence, as determined by the attention weights.

Encoding / Decoding
- The encoder in a Transformer processes the input sequence, applying self-attention and feed-forward layers to capture the representation of each word in the context of the entire sentence. The encoder's role is to understand the input sequence.
- To generate output sequences, Transformers use a technique called "decoding" which involves predicting one output token at a time based on the previously generated tokens. The model uses a mechanism called "masked self-attention" to prevent it from attending to future tokens that it should not yet have access to.

Positional encoding is used in Transformers to provide information about the position of each token in the input sequence. This is important because the self-attention mechanism only considers the relationship between tokens, but does not take into account their absolute position in the sequence. Positional encoding allows the model to encode this information in a way that is compatible with the self-attention mechanism.. Since Transformers don't have the notion of word order by default, positional encoding helps them understand the sequential order of words in a sentence.

In a Transformer model, the input sequence is processed sequentially, one token at a time. At each step, the self-attention mechanism allows the model to attend to all the previous tokens to capture their relationships. However, it does not take in the entire sequence at once.

Transformers handle variable-length input sequences by using a technique called "padding" to ensure that all input sequences have the same length. This involves adding special tokens (e.g., zeros) to the end of shorter sequences to make them the same length as the longest sequence in the dataset. The model then uses a mask to ensure that it does not attend to the padded tokens during processing

Archetecture:
- Transformer layers are the building blocks of the Transformer architecture. Each layer consists of two sub-layers: the multi-head self-attention mechanism and the position-wise feed-forward neural network. The self-attention mechanism allows the model to attend to different parts of the input sequence simultaneously, capturing dependencies between words. The feed-forward network applies a set of linear transformations to each position in the sequence independently, enabling the model to learn complex relationships. Stacking multiple transformer layers allows the model to capture different levels of representation and abstraction in the data.
- Here's an example to help illustrate the concept: A Transformer model may consist of multiple encoder layers and multiple decoder layers. Each encoder layer processes the input sequence independently, and its output is passed to the subsequent encoder layer. Similarly, each decoder layer takes the output of the previous decoder layer as its input. The depth of the Transformer architecture, achieved by stacking multiple layers, enables the model to learn hierarchical representations of the input data.

Masking
- During the subsequent processing steps, the Transformer uses attention masks to prevent it from attending to the padding tokens. The attention masks essentially indicate which parts of the input should be attended to and which parts should be ignored. By applying these masks, the Transformer focuses only on the meaningful parts of the input sequences, disregarding the padded tokens.
- Attention masking is used to prevent each word from attending to all other words, except for those preceding it. This restriction helps reduce the computational complexity. Additionally, if a sequence is very long, it can be divided into smaller "chunks" or segments, allowing the model to process the sequence in parts and aggregate the information.

Transformers have been used in a wide range of applications, including natural language processing, speech recognition, and image captioning, among others. The most well-known example of Transformers is the BERT (Bidirectional Encoder Representations from Transformers) model, which has achieved state-of-the-art performance on a wide range of natural language processing tasks.

Multi-head attention in Transformers refers to the idea that attention is computed multiple times in parallel, each time with a different learned linear projection. This allows the model to attend to different aspects of the input simultaneously, capturing different relationships and dependencies. The outputs of the multiple attention heads are then concatenated and linearly transformed to produce the final attention output.

Encoder and Decoder:
The encoder in a Transformer processes the input sequence, applying self-attention and feed-forward layers to capture the representation of each word in the context of the entire sentence. The encoder's role is to understand the input sequence. On the other hand, the decoder generates an output sequence based on the representation learned by the encoder. It also utilizes self-attention but additionally incorporates encoder-decoder attention to attend to the relevant parts of the input during the decoding process.

Skip Connections / Residual Connections: Like [[Resnet]] transformers use skip connections to remember data from previous layers.

Residual connections in Transformers contribute to their effectiveness by allowing the model to retain important information from previous layers during the training process. The residual connections bypass the layer and add the input of the layer directly to its output, which helps alleviate the vanishing gradient problem and allows for easier flow of gradients during backpropagation. This way, the model can effectively capture both low-level and high-level features in the data, leading to improved performance.

Loss Function
- The loss function in training Transformers measures the dissimilarity between the predicted output sequence and the ground truth (target) sequence. It quantifies how well the model is performing in generating the desired output. By comparing the predicted output to the target sequence, the loss function provides a measure of the model's performance, and during training, the model adjusts its parameters to minimize this loss. Commonly used loss functions for sequence generation tasks include cross-entropy loss and masked language modeling loss.


Optimization Algorithm

Why Transformers Good:
Skip connections 
Attention Masking

Why they are bad:
Needs ton of data
Bad with rare words
Bad with long sentences comprehension
Computationally expensive

[[Unsupervised Learning]]
