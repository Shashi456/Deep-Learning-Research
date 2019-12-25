# CTRL - A Conditional Transformer Language Model for Controllable Generation
## Summary 
- Recent advances in LM have allowed for generation of coherent text, but they don't allow for 
  controlling aspects of generated text. 
- CTRL is a LM conditioned on a variety of control codes which specify domain, style, topics, dates, entities and the relationships between them, plot points and task related behaviour. CTRL always conditioned on p(x|c) where c is the control code. 
- Trained on 140GB of data including Wikipedia, Project Gutenberg, around 45 subreddits, OpenWebText, Europarl etc. 
- Controllable Generation :
  - Introduce penalized sampling, which trust the model distribution through near-greedy sampling but penalizes for repetition. (Similar to coverage in See et al, Welleck et al).
  - Control codes: Allow stylizing generated text by domain, complex codes can be made by appending these codes to the domain code. Task specific codes are allowed as well. 
  
  
## Strengths 
- Having control codes for having power over what kind of text you want to generate is a novel idea.
- The model seems to make a lot of relations within control codes as well.

## Questions
- Can this be used as a finetuned model for a downstream task? Can we still say that this model is learning representations on some level?
