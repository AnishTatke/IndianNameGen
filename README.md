# Indian Name Generator

This project implements Andrej Karpathy’s infamous MakeMore series on Indian Names. The project implements three approaches to generate new first names using various parameters, optimization techniques and model implementations as the MakeMore series explains.

All rights and credits for code and idea implementations belong to respect authors. This project is completely coded for research and learning purposes. Big thanks to Andrej and his brilliant compilation of MakeMore series which helps students like myself to understand and experiment with Language models and Deep Learning Optimization Techniques.

## Datset
The Indian Names Dataset is is custom dataset generated from combining two Kaggle dataset as provided below.

1. https://www.kaggle.com/datasets/ananysharma/indian-names-dataset
2. https://www.kaggle.com/datasets/jasleensondhi/indian-names-corpus-nltk-data



- __Bigram Model__
    - This model is based on simple counting and probability of next word based on the immediate previous words. The idea is extended to optimizing a Negative Likelihood Loss that helps in generating newer words.
- __Bag of Words MLP model__
    - This model extends the Bigram model by implementing “context length” based Bag of Words model inspired from [1]. It explores custom implementations of PyTorch’s `nn`  layers and training a model on various hyperparameters. Various intermediate model layers such as activation layer outputs are analyzed statistically and visualized for learning purposes. The inference is that this model optimized the loss achieving a new benchmark on Indian Names dataset and generates better Indian names.
- __Wave Net inspired Model__
    - Inspired from the Wave Net [2] implementation, this model hierarchically combines the embedding of every two characters for a context length of 8 and consecutively repeats the same in the forward pass until the last layer. Again, a new benchmark of optimization and loss is achieved in this model.
    



## References:

1: Operationnelle, Departement & Bengio, Y. & Ducharme, R & Vincent, Pascal & Mathematiques, Centre. (2001). A Neural Probabilistic Language Model. 

2: Oord, A. V., Dieleman, S., Zen, H., Simonyan, K., Vinyals, O., Graves, A., Kalchbrenner, N., Senior, A., & Kavukcuoglu, K. (2016). WaveNet: A Generative Model for Raw Audio. *ArXiv*. /abs/1609.03499