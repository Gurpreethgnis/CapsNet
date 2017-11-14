# CapsNet or Capsule Networks

Sabour et al. 2017: "A capsule is a group of neurons whose activity vector represents the instantiation parameters of a specific type of entity such as an object or object part."

Capsule Networks are made of these capsules that offers the state-of-the-art performance for MNIST character recognition dataset. They are an improvement to the convolutional neural network because of the two following reasons

1.  They understand the spatial relationships between the set of features whereas in the case of convoutional neural networks while subsampling/ pooling this information is lost.
2.  They are more robust to the geometric transformations of the learned features such as rotation, translation etc. Hence these are more generalisable. 

Capsule Networks have many layers nested inside a layer that is called a capsule. Capsule networks are different from Convolutional neural networks (1) In the manner that they are connected i.e. architecture of the network and (2) the way the information is routed through the entire network. Both of these have been briefly described below

1. Squashing - Architecture of the network and their activation  

In the case of CNN we make use of activation functions such as ReLU (Rectified linear unit), tanH (Hyperbolic Tanget), Sigmoid function etc. to decide which of the layers are important to be "activated. That is, we apply these activation functions to each layer of the CNN to determine that for a particular feature in the input image whether this layer has an important contribution to the next layer or not. Thus as the layers become deeper, use of activation function such as ReLU is more efficient then tanH or sigmoid function as the former is computationally less expensive. 

In the case of CapsNet, as a number of layers are clubbed together into capsule. So in this case, instead of applying a non-linear function to each layer inside the capsule, a "squashing" function is applied to the output of the capsule.  

2. Routing: 

In the case of CNN, maxpooling determines the flow of information between the layers. As discussed above, pooling leads to loss of information about the spatial relationship between the set of features in an image as the output of the max pool layers ia a scalar quantity.

In the case of CapsNet, a new routing mechnanism has been proposed. The output of each capsule is a vector quantity. Hence, this preserves the spatial relationship between the features in an image.

Links for discussion forums

https://www.reddit.com/r/MachineLearning/comments/78zvc4/r_171009829_dynamic_routing_between_capsules/






Links for informative videos

Capsule Networks: An Improvement to Convolutional Networks By Siraj Raval : https://www.youtube.com/watch?v=VKoLGnq15RM and the code for the tensorflow implementation of the same is available at 
