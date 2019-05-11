# Weights-and-Unit-Neuron-Pruning

In this project, my aim is to train a large neural network and then prune it to understand how the accuracy of the NN is
affected as more and more of it pruned. Pruning here effectively referes to increasing sparsity in the network, and given a
neural network layer, pruning can be performed in 2 ways:

1. Weight pruning: set individual weights in the weight matrix to zero. This corresponds to deleting connections between the
neurons of consecutive layers. Here, to achieve sparsity of k% we rank the individual weights in weight matrix W according
to their magnitude (absolute value) |w(i,j)|, and then set to zero the smallest k%.

2. Unit/Neuron pruning: set entire columns in the weight matrix to zero, in effect deleting the corresponding output neuron.
Here to achieve sparsity of k% we rank the the columns of a weight matrix according to their L2-norm & delete the neurons with  smallest k% norms.

Naturally, as we increase the sparsity and delete more of the network, the task performance will progressively degrade.

In this project, I plotted the accuracy vs sparsity plots for both weight pruning and neuron pruning.
