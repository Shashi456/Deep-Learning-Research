# Parameter Selection: Why We Should Pay More Attention to It
- An opinion paper on the importance of parameter selection while training neural network models.
  - The process remains challenging due to the huge number of parameter combinations
- MultiLabel Classfication for medical code prediction task ->  predict the associated ICD (International Classification of Diseases) codes of each medical doc- ument.
  - MIMIC-III Full and MIMIC-III 50, Mullenbach et al[1] tunes parameters for the full dataset but when its the 50 labels 
  they dont tune parameters and apply the same. 
  - A lot of works copy Mullenbach's parameters on the 50 label MIMIC dataset and showcase superior performance, but parameter
  tuning the original model makes Mullenbach's model surpass most of the subsequent work.
<img width="537" alt="image" src="https://user-images.githubusercontent.com/18056781/125390436-83d60780-e3c0-11eb-9372-f8190022ab52.png">
- The authors do a grid search of parameters and finetune both the models presented in Mullenbach et al, acheiving better results.
- This investigation showed that if resources or time are available, more attention should be paid to the parameter selection.

 






[1] - https://arxiv.org/pdf/1802.05695.pdf
