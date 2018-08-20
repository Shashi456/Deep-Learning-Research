# Intriguing properties of Neural Networks 

## Summary 
- This paper primarily discuss two properties of neural networks.
- Property one: Semantic meaning of individual units.
  - Visually inspecting images which maximize the activation of various units in the natural basis direction and of images which 
  maximize the activation of various units in a random basis give rise to similarly interpretable semantic properties. 
  - This leads us to conclude that the semantic information is contained in the space rather than the individual units when it comes to
  the higher levels of the neural network.
- Property two: Stability of neural networks with respect to small perturbations to their inputs.
  - Consider a state of the art DNN that generalizes well on object recognition, although we may expect the neural network to be robust to
  small perturbations. It is found that a non-trivial filter(perturbation) can arbitrarily change the network's prediction. These are 
  called adversarial examples.
  - Although CV models have employed input deformations during training for robustness these deformations are statistically inefficient, 
  they are highly correlated and are drawn from the same distribution throughout the entire training of the model.
  - It is observed that these "adversarial examples" generalize over models and different data subsets.
 
## Strengths 
- Establishes existence of adversarial examples and a way to generate adversarial examples.
 
## Weaknesses
- Little mention of how these adversarial examples are formed.
