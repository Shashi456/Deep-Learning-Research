# Explaining and Harnessing Adversarial Examples

## Summary 

- This Paper explains why Adversarial Examples are formed.
  - Previous Attempts included complex explanations like Non Linearity, Insufficient Model Average and Insufficient Regularization.
  - It is shown that linear behaviour in high dimensional planes is sufficient to cause Adversarial Examples.
  - This explanation allows the Authors to design a fast method of generating adversarial examples.
  - One of the major reasons is the perturbations is smaller than the precision of the input feature.
  - They observe that cheap algos are able to generate misclassified examples and hence this serves as evidence for their 
  assumptions on how adv. examples are formed.
- Hypothesizes that neural network is too linear to resist linear adversarial perturbation.
- They describe a method for Adversarial Training.
- Shown that Adversarial Training can result in regularization. 
- RBF networks are resistant to adversarial examples.
   
## Strengths and Future Questions 
- Finding models which resist adversarial examples but also maintain state of the art accuracy on clean inputs
- Ian Goodfellow in this paper explains why adversarial examples are formed in a simpler way compared to previous attempts.
- There's a tradeoff between models that are easy to train due to their linearity and models that use nonlinear effects to resist adversarial 
perturbations. One way to go beyond this trade off is to design more powerful optimization methods.
- Finding Models which may be just moderately difficult to optimize but very hard to perturb.

## Weaknesses & Doubts
- Assumption that linear nature is completely responsible for Adversarial Examples.
- No consideration of NNs which have no simplifying to display linear properties.
