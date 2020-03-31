# Attention is all you need

## Summary

- Proposes a new network architecture based solely on attention mechanisms, dispensing with recurrent units and convolutions.
- Recurrent models inherent sequential natures precludes parallelization within training examples which becomes critical at longer sequence lengths, the transformer architecture eschews recurrence and entirely relies on an attention mechanism(self-attention) to draw global dependencies between input and output.
- The architecture :
  - The encoder is composed of a stack on 6 identical layers, each layer has two sublayers. The first is a multi-head self attention
  mechanism and the second is a simple position wise fully connected feed-forward network. A residual connection followed by a layer 
  normalization is employed around the sub layers.
  - The decoder also has 6 identical layers, in addition to two sub layers there exists a sub layer which performs multi head attention 
  over the output of the encoder stack. The same additions are employed around these layers.
- The scaled dot-product attention is employed which is faster and space efficient while at the same time a scaling factor is used in order 
to counteract effects of dot-product attention, can be thought of as taking the good properties of dot-product attention and counteracting 
the negatives to make its performance comparable to additive attention.
- Multi head attention "allows the model to attend to information from different representation subspaces". 

## Strengths
- Introduces a new pure attention-based network architecture which achieves state of the art performance.
- Faster to train. 
- Self attention allows the model to be more interpretable. The attention in the model mimics that of typical encoder-decoder models, the encoder and decoder can attend to all positions in the previous layer.  
- Achieves state of the art performance in WMT tasks.

## Weaknesses/ Doubts
- How can the interpretability be understood?
- Can character transformers be made like char-RNNs/char-LSTMs?
