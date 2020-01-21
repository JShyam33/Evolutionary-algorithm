# Evolutionary-algorithm
Evolutionary approach to train CNN on MNIST dataset


Inspired by this https://towardsdatascience.com/evolving-neural-networks-b24517bb3701 Medium article I recreated the code for first part to train a simple fully connected network for regression.

All the code for first is from blog only

for second part i created my own model and applied CNN from scratch to train MNIST dataset.
I first created the CNN using keras API and train it with full dataset for 12 epochs and got 99.23% test accuracy.

Then i implemented Evolutionary approach

Instead of conventional aproach like back propogation this method takes inspiration from theory of evolution of species. 
all neural networks are organisms and each are initialized randomly from normal distridution. we pass images and get the output, the network with best scores survives to the next generation. we create new newral networks by combining weights of two best networks. we randomly mutate the weights of neural network. Thus by natural selection we find the best neural network for the job.

It takes more time than keras model due to initialization and combination of weights so for simple task it may not be useful. I emphasize more on the method then on result as there are many things we can do to improve the chance to find best network like increasing population size, trying different initializations also i have fixed the structure of the network to decrease the complexity. 

To understand deeply on the evolutionary algorithm i would suggest reading this blog. https://towardsdatascience.com/evolving-neural-networks-b24517bb3701.
