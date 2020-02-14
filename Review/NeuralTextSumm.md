# Neural Text Summarization: A Critical Evaluation
- This paper does a critical evaluation of the research task of text summarization on the basis of datasets, evaluation metrics an models.
- It is found that :
  - automatically collected datasets leave the task underconstrained and may contain noise detrimental to training and evaluation.
  - Current evaluation protocols aren't closely related to the human idea of summarization.
  - Models overfit over the biases of the datasets.
- The current setting in which models are trained with one reference summary and no additional info, leaves the task of summarization underconstrained. Unconstrained writing leads to more verbose summaries which might not necessarily add information.
- News articles suffer from a position bias.
- Datasets have noisy examples and these should be filtered out by using simple regular expressions and heuristics.
- Summaries are rated on relevance, consistency, fluency, coherence. Rouge scores are a very poor notion of summarization.
