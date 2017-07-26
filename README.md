# Deep-learning nanodegree 

This repository contains all projects I finished as part of Udacity's deep learning nanodegree.

![neural-networks1](https://user-images.githubusercontent.com/22200326/28597802-3de678e0-71a0-11e7-94b8-6ceef91cfd30.png)


# 1. My first neural network 

In my first project I developed a simple neural network from scratch in raw numpy to estimate the most optimal price per unit for a bike store, in relation to the bike's prices and the amount of clients.

# 2. Image classifier 

Next I implemented an image classifier as a convolutional neural network inspired by alexnet's architecture which was trained on the CIFAR10 dataset, achieving a 70% accuracy.

![convolutional-networks](https://user-images.githubusercontent.com/22200326/28600440-3d5bb43c-71b2-11e7-9836-84f9d502ca5a.png)
It consisted of a classical architecture, defined by two convolutions with dropout layers and two fully connected layers.

![08-alexnet-1](https://user-images.githubusercontent.com/22200326/28600444-43e89bbc-71b2-11e7-9152-db7b5cc999fb.png)

Around 2011, a good classification error rate was 25%. In 2012, a Alex Krizhevsky's convolutional neural net achieved 16%; in the next couple of years, error rates fell to a few percent. By 2015, researchers reported that software exceeded human ability at narrow visual tasks.

# 3. TV script generator 

Diving deeper into recurrent neural networks, I designed a sequence to sequence model, with encoders and decoders implemented as LSTM cells, lookup tables and embeddings to boost performance and clean the data, filtering out the noise.

LSTM stands for long-short term memory; an LSTM cell allows the model to keep track of previously processed data. 
The cell processes and input and a previously stored value, which comes as an output to a sigmoid function, if the value given as output is equal to zero the current input won't be processed since they both are being multiplied.

![lstm](https://user-images.githubusercontent.com/22200326/28600459-601ffbcc-71b2-11e7-8b97-2a5ecfe42a3d.jpg)

It will pass the information as long as it is relevant, using an attention layer that filters out the words whose probability to appear is lowest, in order to keep track of context.
The generated scripts are still non-sensical, with some days of training and more data it would have given more impressive results, the adjustment of the hyperparameters was enough for the model to offer a smooth drop in the loss function, and RNN's usually run better with three layers but any more than that will result in a plateu effect according to Ian Goodfellow's papers. CNN's on the contrary give room for as many layers as are necessary.

# 4. Language translation 

By far my favourite project, a sequence to sequence model was trained to translate from english to french, the accuracy went well beyond 90% giving really impressive results. 
More data would have made it easier to improve the model. 

![seq2seq](https://user-images.githubusercontent.com/22200326/28600461-670e2882-71b2-11e7-98af-60e61e7584f8.png)

# 5. Face generation 

Generative adversarial networks or GAN's consist of two convolutional neural networks a generator and a discriminator which as part of a probabilistic model give us machine-generated results. 

![dcgans](https://user-images.githubusercontent.com/22200326/28600533-e4bbba56-71b2-11e7-87e7-f739fa55190e.png)

The idea underlying this concept is that the generator creates data whilst the discriminator tries to classify it as fake or real data, as both generator and discriminator get better at their tasks,
more accurate outputs are being given.
A sigmoid cross entropy function is being used for both losses to drop.
In my project I designed a GAN trained on celebrities' pictures that eventually learnt to generate faces.

![gans](https://user-images.githubusercontent.com/22200326/28600538-e955e078-71b2-11e7-8690-bfeb8e67998a.png)

GAN's follow an architecture similar to that of RNN's but the convolutions in this case are ordered
by increasing size.

![gans](https://user-images.githubusercontent.com/22200326/28600538-e955e078-71b2-11e7-8690-bfeb8e67998a.png)


