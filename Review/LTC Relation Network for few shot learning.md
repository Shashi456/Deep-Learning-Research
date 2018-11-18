# Learning to Compare: Relation Network for Few shot Learning

## Summary 
- The paper suggests a novel architecture for one-shot, few-shot and zero shot learning performing state of the art at the time the paper was 
published. 
- The Network is two fold, first the query images and training images are passed through a CNN to create feature representations which are then 
concatenated andfed  into the relation network which determines if they are in the matching category or not.
- The dataset is split in such a way that the network can first be trained in order to perform meta-learning on the training set and this also allows to learn transferable knowledge(Coudld be though of as somewhat similar to transfer learning in CNN) for performing well in one shot learning. 
- Previous one shot learning methods used pre-specified metrics like euclidean or cosine to perform classification so they can be thought of as
a distance metric learning. While in the relation network, first an embedding of the features is learned and since no distance metric is specified, the network is also learning a similarity function. This allows the network to learn a distance metric in a data-driven way. 


## Strengths and Further Research 
- The paper suggests a state of the art novel architecture. 
- Is one shot learning oblivious to Adversarial Examples, can they be fooled?

## Weaknesses and Doubts
- How exactly can we think about the distance metric that is being learnt by the network ?
- Can One shot learning be used for normal classification purposes? Would that be free of Adversarial Examples?
