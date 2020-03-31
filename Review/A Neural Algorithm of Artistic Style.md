# A Neural Algorithm of Artistic Style

## Summary 
- Using Neural Networks to create artistic images of high perceptual quality, The way it is done is by separating content and style of 
arbitrary images. This ultimately leads to the development of a Neural Algorithm.
- Along the processing hierarchy of a Convolutional network, the input image is transformed into representations which resemble the actual
content of the image compared to the detailed pixel values. The deeper the layer gets the higher the level of content it represents in 
terms of objects and arrangements in the input image. Therefore the feature responses in the deeper layers are called "content 
representation". The style of an input image is built on top of the filter responses in each layer of the network.
- Image Content and Style cannot be completely disentangled.
- Using Neural Networks trained on object recognition, manipulations in feature spaces that explicitly represent the high level content of 
an image are carried out.
- Provides an Algorithmic Understanding of how neural representations can independently capture the content of an image and the style in
which it is presented.
- The style representation is calculated with gram normalization.

## Strengths
- A key finding of the paper is that the representations of content and style in a CNN are separable.
- Provides a tool to study perception and neural representation of art, style and content-independent image.
- The way it is found out that a neural system which is trained to perform a core computational task in biological vision also 
automatically learns image representations of content and style is fascinating. I think this paves a way in not just being able to perform
a different task but also interpretability.


## Weaknesses and Doubts
- Is Attention Based Style Transfer Possible, certain parts of the image are converted to a different style but still the image 
holistically looks meaningful?
