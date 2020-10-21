# On the Abstractiveness of Neural Document Summarization
- The paper attempts to verify the degree of abstractive based on the overlap in terms of various types of units.
- Many neural news summarizes (till see et al/paulus et al) which claimed to be abstractive tend to directly copy large spans of contents from the original documents.
- They experiment with crating a seq2seq model (within the pointer-generator model) which uses the soft attention distribution to produce an output sequence whose elements are all from the input sequence, similar to a pointer network.
    - Upon evaluating this model over informatives, relevance, fluency and coherence, they found that this experimental copy system performed similarly to the pointer-generator