# Neural Text DeGeneration with Unlikelihood Training
## Key points
- Standard likelihood training and decoding leads to dull and repetitive outputs. This paper aims to solve the problem of generation at the training level instead of decoding techniques like Nucleus sampling [Helmholtz et al 2019](https://arxiv.org/abs/1904.09751). 
- This paper shows that the likelihood objective might be at fault and proposes a new objective unlikelihood training which forces unlikely generations to be assigned lower probabilities. 
- Two major flaws of the likelihood objective are it pays relatively little attention to the argmax of the "next probabilistic tokens" and it is not optimizing sequence generation.
- Unlikelihood training can work on the token level and the sequence level. it assigns a lower probability to tokens which dont generally occur but are assigned too high a probability. 
- Since, the problem of finding the optimal continuation to a sub sequence/ prefix of a particular sequence is not tractable, we choose to use decoding strategies like deterministic decoding and stochastic decoding. 
- Deterministic decoding strategies include those of greedy and beam search while stochastic decoding include those of top-k and nucleus sampling. 
- There are two issues which general occur in neural language models:
    - Repetition : It's found that average n-gram repeated in model continuations with greedy decoding (43%) compared to humans (0.5%), and that next predicted next tokens that appeared in the last 128 tokens occured 62% of the time in TLMs against 49% in ground truth text. 
    - Token Distribution mismatch. 
- The unlikelihood loss incorporates, the idea of using negative candidates and minimizing their log probabilities, for the candidates previous context tokens are used, this achieves two things incorrect repeating tokens less likely and frequent tokens less likely. 
- In sequence level unlikelihood objective, negative candidates are to penalize repeating n-grams. 
- The sequence level unlikelihood objective can be used as a finetuning training objective after originally training on the MLE objective, or it can be used in conjunction with the token level objective. Even with the finetuning objective, unlikelihood training shows substantial gains. 