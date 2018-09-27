# Universal Language Model Fine Tuning for Text Classfication 

- Addresses Lack of Inductive transfer learning within NLP, although word embeddings like word2vec exist, they only target a model's 
first layer. 
- Propose ULMFit a method that can be used to achieve CV-like transfer learning for any task.
- ULMFit has three stages:
  - General Domain LM pretraining: Language Model trained on a general domain corpus to capture general features of the
  language in different layers.
  - Target task LM fine-tuning: The Full Language Model is fine tuned on target task data using Discriminative fine-tuning
  and slanted triangular learning rates.
  - Target task classifer fine-tuning: The classifer is fine-tuned on the target task using gradual unfreezing, and the 
  methods used in step 2.
- Discriminative fine tuning can be simply thought of as having different learning rates for each layer being fine-tuned.
- Slanted triangular learning rates includes first increasing the learning rate linearly and then decays linearly as well. 
- 
