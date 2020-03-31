# Sequence to Sequence Learning with Neural Networks

## Summary 
- Provides a general end-to-end approach to sequence learning.
- Introduces a new class of "Encoder-Decoder" architectures for the seq2seq learning.
- A straightforward LSTM architecture can be used to solve general sequence to sequence problems.
  - The idea to is use one LSTM to read the input sequence, to obtain some sort of "encoding".
  - This encoding is then used by another LSTM to extract the output sequence, this can be thought of as the decoder, which is basically a 
  rnn language model which is conditioned on the input sequence. 
  - LSTMs are used because they can handle long range temporal dependencies and also can map variable length inputs to fixed dimensional 
  vector representation.
  - The inputs are given in the reverse order to create short term dependencies and a special end of sentence symbol is needed.
- This architecture performed state of the art performance in 2014 on the english to french translation task by WMT, The LSTM did not 
suffer on longer sentences.


## Strenghts
- Introduces Seq2Seq Learning using LSTMs to Deep Learning.
- The ability to turn sentences into a fixed-dim vector helps in visual representation and see if the model is able to "learn" semantic 
properties.

## Weaknesses and Doubts
- Interpretability of the output of the encoder, How can this "fixed dimensional vector" be interpreted and can this be thought of as a 
sentence embedding?
- There is no clear explanation to reversal of input.

