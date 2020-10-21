# Information-Theoretic Probing with Minimum Description Length - Lena Voita and Ivan Titov
- Alternate Titles: What happens when relations between alice and bob have gone too far?
- What is going on in NLP?
    - Pretrained models 
        - have huge impact and popular
    - Analysis of these models is important
- How to understand if a model captures a linguistic property?
    - How to understand if representations x<sub>1:n</sub> encode y_1:n

- What is going to happen
    - Standard approach: probing classifiers
        - Standard Probing: train a classifier, use its accuracy?

    - Some "sanity checks"
        - Model (Classifier): Trained vs random 
            - very close accuracies 
            - to see differences, had to reduce training data
        - Labels: Linguistic vs random 
            - 
    - Standard approach: is to train classifier, 
        - its been shown there are issues
            - random as good as trained
            - encode random labels 
    - Information-Theoretic point of view\
        - Look at this problem from a information theoretic perspective
        - REgularity can be used to compress the data
        - better compression -> stronger regularity -> representation better encode labels
        - The probing classifier can be a compression algorithm
        - Changing goals from 
            - Goals: predict labels -> transmit data
            - probe: standard -> MDL probe 
            - Measure: accuracy -> code length (theoretical)
        - The above changes the model from final quality -> Final quality + how "hard" it is to achieve it  

        - minimum description length of labels knowing representations -> MDL probes
            - Can be found from a model which models p(y|x)
        - Cross-entropy is the data codelength
            - Shannon-Huffman code: there exists a code to compress labels losslessly with a codelength
                - the bound is optimal if data is independent and model is p(y|x)
            - this would mean learning is compression
                - For K classes, uniform encoding assumption
                - Uniform codelength
        - How hard is it to achieve it ?
            - Strength of regularity in the data
                - Better compression means stronger regularity 
                - can be understood with "less effort"
                - can be explained with a simple rule
                - can be revealed with a few examples
            - This is how amount of "effort" is translated into codelength
        
    
    - Variational Code: An instance of two-part codes
        - Transmit model weights explicitly
        - Weights with higher variance can be transmitted with lower precision
        - With variational methods, can use different priors
            - Bayesian Compression
        - Two ways to assess probe complexity
            - Codelength
            - Pruned architecture
    - Online Code:    
        - Transmit model weights implicitly
    - The previous way of reducing probe size can be thought of as indirectly manually to account for      
      variational code for amount of effort while reducing the amount of probe training data is can be thought of as indirectly manually accounting for online code for amount of effort
        - MDL does this directly and is theoretically justified.
    - Experiments
        - Check paper 
    - For linguistic task, best layer is the first and large difference between layer 0 and contextual representations
    - For control task, 
        - scores becomes larger as we move up 
        - code length for control task is higher 
    - What was unexpected 


    - What was important on the way
    - Specially for friends
        - Unexpected agreement between the codelengths 
            - Description length of deep learning models Neurips 2018 (blier and ollivier)
                - models: convolutional networks
                - variational methods are much worse than online
            - In this authors work, variational vs online, the same compression bounds and same quality
        - How did we come to MDL?
            - Trained models better "encode" linguistic properties 
            - to define "encode" more formally?
                - sentiment neuron, open ai
                    - a very small model is enough to extract sentiment
                    - a few examples are enough to learn how to extract sentiment
                - corresponds to strong regularity 