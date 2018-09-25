# Neural Machine Translation by Jointly Learning to align and translate

## Summary
- Since the usage of a fixed-length vector is supposed to be a bottleneck for seq2seq learning, this paper suggests allowing a model to
automatically search for parts of a source sentence that are relevant in predicting a target word.
- Instead of attempting to encode the input sentence into a single fixed-length vector, it encodes the input sentence into a 
sequence of vector and choose a subset of these vectors adaptively while decoding. 
- Not squashing a sentence regardless of length into a fixed length vector helps this model to cope better with long sentences.
- They suggest a new architecture which comprises a bidirectional RNN as an encoder and a decoder that emulates searching through
the source sentence while "translating".
  - The Bidirectional RNN is used to create an annotation which contains the summaries of both preceding and the following words.
- Their architecture is more robust to length of sentences.


### Neural Machine Translation [Digression]
- It is equivalent to finding a target sentence y that maximizes the conditional probability of y given a source sentence x.
- Once the Conditional distribution is learned, a source sentence can be translated into a target language by searching for a 
sentence which maximizes the conditional probability.

## Strengths
- Provides an intuitive way to inspect alignment betwen the words in translation and the source sentence. 
- Naturally deals with variable lengths of source and target phrases.
- Can handle longer sentences because only accurately need to encode parts of the input sentence surrounding a particular word.
- Provides a way of "Attention" in Neural Translation.

## Weaknesses/ Doubts
- How does this attention scale to very long sentences? Is there a need to break paragraphs down into long sentences?
- Does attention capture context in any way? can these position based word annotations can be thought of as context embeddings?
