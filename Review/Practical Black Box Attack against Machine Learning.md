# Practical Black Box Attacks against Machine Learning

## Summary 
- This paper considers questions like practicality in the adversarial attacks. 
  - Previous Adversarial Example Attacks assume knowledge of the entire model or training data, which is hardly the case in real world
  applications.
  - This paper describes the first practical demo of attacking an adversary remotely hosted, the attacker has no knowledge of the architecture or the dataset.
  - They propose a two-step method for the attack, training a local substitute and then using the local substitute for generating adversarial examples.
- Training a local substitute includes creating a synthetic dataset, while the outputs are labels assigned by the target DNN. 
  - The synthetic dataset is created by jacobian based heuristic.
  - It is found that the architecture of the local substitute doesn't affect the performance of generating adversarial examples.
- Generating adversarial examples is done by two methods Goodfellow algorithm or the Papernot algorithm.
- Validation of the attack is done by attacking Metamind, Google and Amazon DNNs which misclassify 84.24%, 96.19% and 88.94% of the generated adversarial examples respectively.

## Strengths and Future Questions
- Transferability of Architecture is a new avenue to explore. 
- The paper combines three properties which are the capability being limited to observing output labels, the number of labels queried is limited ( because extensive querying would lead to detection of adversary) and the approach scales to different ML classifier types.
