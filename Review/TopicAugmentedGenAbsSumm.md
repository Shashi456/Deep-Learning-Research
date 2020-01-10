# Topic Augmented Generator for Abstractive Summarization
## Summary 
- The paper introduces a new decoder where the output summaries is generated by conditioning on both the input text and the latent topics of the document found through LDA. The decoder is also availed with word co-occurence statistics. 
- To generate a word, the generator learns to switc between conditioning on text or latent topics or directly copy the word. 
- The decoder is to be biased towards generating words reflecting underlying latent semantic information. 
- The model is evaluated on CNN/Daily Mail and Wikihow. 

## Strengths 
- The model seems to perform decently, giving some proof for the need of having other article/document level semantic information for the generation of summaries. 

## Weaknesses/Doubts
- Is LDA the best that can be done for topic modeling? 