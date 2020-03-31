# Query Based Abstractive Summarization Using Neural Networks
## Summary
- This paper shows that existing Neural network models can be constructed upon to make use of queries to produce summaries. They show this by training a pointer generator.
- The model is designed for brief summaries, mostly single sentence.
- Summarizing with respect to a query is somewhat similar in idea to topic, which asks the question "What is the summary of the document with respect to query X?"
- There is a document and query encoder respectively, the outputs are then passed to an attentive decoder which generates a summary. The encoder and decoder are GRU RNNs.
<img src='../Images/QBNN.JPG'>
- There is a loss for the pointer mechanism, the attention mechanism and the generation mechanism, which is added and normalized by the length.
- Summaries are decoded using beam search.
- A dataset is constructed of the original CNN/DailyMail QA dataset, which consisted of document-query-answer triples. The original method was to use close style questions in which the answer was masked and made to be predicted, in this the inverse is done where the word masked is used as the query and the summary has to be generated.

## Strengths 
- The idea that QA datasets can be looked at as Query Based Summarization is useful for the problem in general. 
- A proof of concept for usage of queries in abstractive summarization. 

## Weaknesses 
- The results are underwhelming, failing to cross even 20 R-1 scores, which makes me wonder if the architecture or the dataset remodeling wasn't suited for this particular task. 
