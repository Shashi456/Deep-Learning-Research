# Transforming Wikipedia into Augmented Data for Query-Focused Summarization
## Summary
- This paper introduces a way to automatically augmented wikipedia articles into a query-focused summarization dataset.
<img src='../images/Wikiref.png'>
- Statement citations are used to align queries and documents, The highlighted statement is the summary, the supported citation is used as the context. Article and section titles are used as the query.
- A BERT based query focused extractive summarization model is also introduced. The model takes the concatenation of the query and the document as the input.
- The sentence are first scored given the query and its salience to the document, then these scores are ranked under constraints like no of sentences and the length of the summary.

## Strengths
- Data augmentation for a Query Based Summarization task is important in a time where summarization datasets are scarce.


## Weaknesses/ Doubts
- An extractive approach for a query based summarization probably suffers from comprehension issues.
- How would the model perform if representations from BERT were used as inputs to an abstractive decoder
