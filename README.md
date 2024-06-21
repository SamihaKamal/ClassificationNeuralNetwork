# ClassificationNeuralNetwork
This is a neural network for image classifaction on the CIFAR 10 dataset
The jupyter notebook sheet goes through each section.

## Architecture
The model consists of a backbone and a classifier, each backbone consists of N amount of blocks.
### Block
The minimum required implementation for each block is one linear/mlp layer predicting a vector a with K elements from input tensor X.
```
a = g(SpatialAveragePool(X)W), where g is a non linear activation function
```
and K convultional layers used to produce a single output.
![image](https://github.com/SamihaKamal/ClassificationNeuralNetwork/assets/95424531/ef89649e-3bb7-45d7-8673-48f36a056166)

### Classifier
The classifier takes the output of the last block as an input and computes a mean feature f.
F is passed onto the classifier.
