# Improving Abstraction in Text Summarization

## Summary 
- This paper seeks to improve abstraction in Text summarization tasks, the way they do this they decompose the decoder into a contextual network which retrieves  relevant parts of the source document and a pretrained language model that incorporates prior knowledge about language generation. 
- They also propose a metric to encourage generation of novel phrases. 
- Decoder : 
  - Factors it into contextual network and language model, The contextual network has the sole responsibility of extracting and compacting the source document where as LM responsible for generation of paraphrases.
- Training : 
  - The policy gradient with rouge metric and a novel abstraction reward that encourages the generation of words not in the source
  document.
  - Novel phrase is defined as one that is not in the source document. 


## Strengths 
- The idea of decoupling decoder tasks and making a contextual and LM works.
