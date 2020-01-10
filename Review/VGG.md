# Very Deep Convolutional Networks for Large Scale Image Recognition
## Summary 
- This papers investigates the depth of convolutional network depth on its accuracy. 
- This paper also showsd the effectiveness of depth even with very small (3
*3) convolutional filters, Ultimately showing it can be pushed upto 16-19 layers for maximal effectiveness.
 - The other parameters of the architecture are fixed and only the depth is experimented with.
 - Having multiple lower receptive fields equates to having one larger receptive field filter, but multiplicity of the lower receptiveness through its non-linearity(relu) allows for decision function to be discriminative i.e finetuned. 
 - There version of Multi GPU training involved, splitting each batch of training into several GPU batches, processed in parallel in each GPU, compute batch gradients, and average them to obtain gradients of full batch.
 - The error classification saturated at 19 layers, although its hypothesized that larger datasets might benefit from even deeper layers. 

 ### Reproducibility details
 - The input to the network is 224*224 RGB image. 
 - The mean RGB value is subracted from each pixel.
 - The image is passed through a stack of conv layers, with a small receptive field, 3*3.
 - The convolution stride is fixed to one pixel.
 - The spatial padding is so decided such that the spatial resolution is preserved after convolution.  The padding is 1 pixel for 3*3 conv layers. 
 - Spatial pooling is done by max pooling layers (5 pooling layers), which follow the conv blocks, but not all conv blocks are followed by max pooling layers.
 - Max pooling is performed over 2*2 pixel window, with stride 2. 
 - Different depths have different stacks of conv layers, ultimately followed by 3 Fully connected layers, the first two FC having 4096 channels and the last one having 1000 since imagenet has a 1000 classes.
 - All hidden layers have the relu activation.
 - The width of the conv layers, starts from 64 in the first layer and then increases by a factor of 2 after each max pooling layer, until it reaches 512. 
 - Batch size, 256. 
 - Glorot (Xavier) Initialization of layers. 


<strong> VGG 19 Arch </strong> \
I/p -> 2x Conv3 64 -> maxpool -> 2x Conv3 128 -> mp -> 4x Conv3 256 -> mp -> 4x Conv3 512 -> mp -> 4x Conv3 512 -> mp -> FC 4096 -> FC 4096 -> FC 1000 -> softmax. 

## Questions to think about 
- What happens when you take the width to 1024?


