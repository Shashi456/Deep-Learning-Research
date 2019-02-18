# Multi Reward Reinforced Summarization

## Summary 
- They address the three aspects of Abstractive text Summarization, which include but are not limited to maintaining saliency, directed logical entailment and non redundancy.
- They address this by having two novel reward functions : ROUGESal and Enatil on top of a coverage based baseline. 
- ROUGESal :
  - Modifies ROUGE metric by up-weighting the salient phrases/words detected via a classifier. 
  - Saliency reward, To learn saliency weights the predictor model is trained on sentence and answer span pairs from SQuAD reading comprehension dataset, where human annotated answer spans for important questions as salient info. 
  - Assign saliency probability to each word, weights to ROUGE matching formulation to achieve ROUGESal score. 
- Entail :
  - Rewards high scores to logically-entailed summaries using a classifier. 
  - Add a length normalization score to avoid misleadingly high entailment scores to very short sentences. 
  - The entailment classifer is trained on SNLI and MNLI and the entailment probability between ground truth and each sentence of generated summary as hypothesis is calculated after which the avg. score acts as the Entail reward.
 - Training : 
  - Policy Gradient Reinforce, Joint cross entropy reinforce loss to maintain readability while optimizing non-differentiable evaluation metric. 
  - To avoid the issue of finding complex scaling and weight balance among reward combinations, They train the rewards in alternating mini batches. 
  
  
## Weaknesses 
- Models also suffer from coherence, fluency issues.
- The saliency classifer accuracy is just ~17% which is very low, for use in reward models, similarly entailment classifier is at 75% and it could be higher. 

## Strengths 
- The idea of alternating mini batch optimizing of rewards is novel, and makes sense. 
