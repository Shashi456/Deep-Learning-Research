# StructBERT: Incorporating Language Structures into Pretraining for Deep Language Understanding
- Extend the Original BERT model by incorporating language structures into pre-training
- Two objectives are added 
    - Word Structural Objective
    - Sentence Structural Objective
- Word Structural Objective -> Right order of shuffled word sequence
    - Maximizing likelihood with of placing the words in the original position
    - They use K=3, trigram is a trade off between task difficulty and effect. 5% of words in a sequence are shuffled (Author Comment).
- Sentence Structural Objective
    - Sequential Order of the sentence i.e predict next and previous.
- Achieves State of the Art on Glue
- The model is both trained from scratch and was also tried as a fine-tuning approach on top of roberta, it achieves state of the art in both of the cases. Displaying its efficacy to be a finetuning approach as well.
- The intuition of word ordering task is from the task of Grammatical error correction, while the intuition of sentence ordering task is inspired from the discourse-level coherence property and causal relationship between the natural sentences. (Author Comment)

- https://iclr.cc/virtual/poster_BJgQ4lSFPH.html
- https://openreview.net/pdf?id=BJgQ4lSFPH