# Siamese Neural Networks for One-shot Image Recognition  


## Summary
- One shot Learning is prediction about data for which little supervised information is available. 
- Firstly, Learn a Neural network that can discriminate between the class-identify of image pairs, which is the standard verification task.
  - Verification Models learn to identify input pairs according to the probability that they belong to the same class or different classes.
  - This model can then be used to evaluate new images, exactly one per class, in a pairwise manner against the test image.
  - The pairing with the highest score according to the verification network is then awarded the highest probability for the one shot task. 
- A Siamese NN consists of twin networks which accept distinct inputs but are joined by a loss function at the top. 
- Siamese Networks were originally made for Signature Verification.
- The idea essentially is to parse the data first to make the image learn feature representations in the character space after which one shot
learning is done, this is basically seeing the distance between the test image and one image each from the c classes we want to classify it 
into. 

## Strengths
- An almost human level classifier is made by this network, one shot learning is extremely important to us because humans learn this way, we 
have a caterogical ability to see objects once and then distinguish them from different viewpoints or from some other object. 

## Weaknesses / Doubts
- Wouldn't exactly call this novel.
- I think the architechture can be experimented.
- Would like to know why it works? In the sense that what is it that the network learns during the initial verification-type learning.
