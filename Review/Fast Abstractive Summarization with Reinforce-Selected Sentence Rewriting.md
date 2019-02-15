# Fast Abstractive Summarization with Reinforce-Selected Sentence Rewriting

## Summary 

- Similar to how humans summarize long documents, the authors propose a hybrid extract-then-abstract approach with policy based RL, taking advantage of both the paradigms.
- They also enable parallel decoding achieving 20x inference speed. 
- It's a coarse-to-fine approach. 
- More novel ngrams than earlier papers, justifying extractor has learnt sentence level saliency and not just copying longer sentences.
- The extractor agent :
  - Learns to select salient sentence or highlights.
  - The extractor avoids redundancy issues because the model has chosen non-redundant sentences, but a final reranker component removes the across sentence repetitions. 
  - A hierarchical model learns the sentence represenations of the document and a selection network selects. [ temporal convolutional model + bidirectional LSTM + pointer network for extraction].
  - The extractor performs a differentiable hard extraction, this behavior comes from the fact that they force zero the extraction prob of already selected sentence so as to prevent the model from repeating those sentences.
- The abstractor agent :
  - Rewrites the salient sentences selected by the extractor.
  - It is encoder-aligner-decoder(with copying), trained on pseudo document sentence pairs obtained via simple automatic matching criteria. 
- Training :
  - Randomly initializing and training end to end doesnt lead to quality summaries. First each sub module is trained with a Maximum likelihood estimatel then the RL is applied to train the mdoel end to end. 
  - The RL has sentence level rewards to optimize the extractor only while keeping abstractor decoder fixed.
  - The RL guided extractor uses A2C, Advantage actor critic, a synchronous variant of A3C.
  - To learn how many sentences to extract, a stop action is added to the action space and a F1-Rouge-1 Score is awarded for performing the end of extraction operation. 
  - To avoid repetition, the tri-gram avoidance during beam search is done and a sentence reranking approach is adopted. 
  - They achieve 38.54 is Rouge-L.
  
  ## Weaknesses
  - To achieve high parallelism, the sentences are individually sent into decoder, this makes the summary look disjoint. 
  - There is no improvement on the abstractor as such.
  
  
  ## Strengths
  - The approach has similarities akin to how humans approach summarization. 
  - One of the few techniques, which shows substantial growth on Rouge-L scores.
  
