# CapsNet or Capsule Networks

![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=plastic)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg?style=plastic)](https://opensource.org/licenses/Apache-2.0)


[Sabour et al. 2017:](https://arxiv.org/abs/1710.09829) "A capsule is a group of neurons whose activity vector represents the instantiation parameters of a specific type of entity such as an object or object part."

Capsule Networks are made of these capsules that have demonstrated the state-of-the-art performance for MNIST character recognition dataset. They are an improvement to the convolutional neural network because of the two following reasons

-  They understand the spatial relationships between the set of features whereas in the case of convoutional neural networks while subsampling/ pooling this information is lost.
-  They are more robust to the geometric transformations of the learned features such as rotation, translation etc. Hence these are more generalisable. 

Capsule Networks have many layers nested inside a layer that is called a capsule. Capsule networks are different from Convolutional neural networks (1) In the manner that they are connected i.e. architecture of the network and (2) the way the information is routed through the entire network. Both of these have been briefly described below

## Squashing - Architecture of the network and their activation  

In the case of CNN we make use of activation functions such as ReLU (Rectified linear unit), tanH (Hyperbolic Tanget), Sigmoid function etc. to decide which of the layers are important to be "activated. That is, we apply these activation functions to each layer of the CNN to determine that for a particular feature in the input image whether this layer has an important contribution to the next layer or not. As the layers become deeper, it becomes computationally expensive to keep all the information about each layer in the network. Thus, an activation function that can help to keep only the main contributors is desirable. In these cases, use of activation function such as ReLU has been shown to be more efficient then tanH or sigmoid function as the former is computationally less expensive. 

In the case of CapsNet, as a number of layers are clubbed together into capsule. So in this case, instead of applying a non-linear function to each layer inside the capsule, a "squashing" function is applied to the output of the capsule.  

## Routing: 

In the case of CNN, maxpooling determines the flow of information between the layers. As discussed above, pooling leads to loss of information about the spatial relationship between the set of features in an image as the output of the max pool layers is a scalar quantity.

In the case of CapsNet, the output of each capsule is a vector quantity. Hence, this preserves the spatial relationship between the features in an image. A new routing mechnanism has been proposed to handle the flow of information between the capsules. The information from each capsule is routed to the next most similar capsule. A simpler analogy is hierarchical tree of the layers.


## Links for CapsNet implementation

- https://github.com/soskek/dynamic_routing_between_capsules
- https://github.com/naturomics/CapsNet-Tensorflow
- https://github.com/llSourcell/capsule_networks
- https://github.com/XifengGuo/CapsNet-Keras
- https://www.kaggle.com/kmader/capsulenet-on-mnist
- https://github.com/gram-ai/capsule-networks


## Links for the some slides and papers

- https://arxiv.org/abs/1710.09829
- http://cseweb.ucsd.edu/~gary/cs200/s12/Hinton.pdf
- http://www.cs.toronto.edu/~fritz/absps/transauto6.pdf

## Link for descriptive websites

- https://blog.acolyer.org/2017/11/13/dynamic-routing-between-capsules/
- https://jhui.github.io/2017/11/03/Dynamic-Routing-Between-Capsules/
- https://medium.com/@Synced/hinton-proposes-capsnet-c04e8cec8bea
- https://medium.com/mlreview/deep-neural-network-capsules-137be2877d44
- https://hackernoon.com/what-is-a-capsnet-or-capsule-network-2bfbe48769cc
- https://medium.com/syntropy-ai/how-do-humans-recognise-objects-from-different-angles-an-explanation-of-one-shot-learning-71887ab2e5b4
- https://medium.com/@pprocks/dynamic-routing-between-capsules-explained-b4277226a467
- https://syncedreview.com/2017/10/27/hinton-proposes-capsnet/

## Links for discussion forums

- https://www.reddit.com/r/MachineLearning/comments/78zvc4/r_171009829_dynamic_routing_between_capsules/
- https://discourse.numenta.org/t/hintons-capsule-and-what-is-wrong-with-convolutional-neural-nets/2899
- https://ai.stackexchange.com/questions/1294/how-does-hintons-capsules-theory-work/1313

## Links for informative videos

- Capsule Networks: An Improvement to Convolutional Networks By Siraj Raval : https://www.youtube.com/watch?v=VKoLGnq15RM and the code for the tensorflow implementation of the same is available at 
- Hinton's Capsule Theory: https://www.youtube.com/watch?v=rTawFwUvnLE&feature=youtu.be
- Hinton's talk on Deep Learning: https://www.youtube.com/watch?v=TFIMqt0yT2I

## Links for CapsNet applications
- https://becominghuman.ai/understand-and-apply-capsnet-on-traffic-sign-classification-a592e2d4a4ea
