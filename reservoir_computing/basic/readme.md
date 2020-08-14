
# Reservoir Computing Basic Elements 

![ReservoirComputing1](https://www.degruyter.com/view/j/nanoph.2017.6.issue-3/nanoph-2016-0132/graphic/j_nanoph-2016-0132_fig_001.jpg)

A Neural Network can be thought as composed of 2 main architectural elements

- a Core, where most of the computation is performed and 

- a Final Layer, which is application specific, as the training signal is stronger 



## Classic ML NN 

The Traditional Neural Networks used in Machine Learning do not show this distinction very clearly as

- everywhere they rely on the same kind of (biologically inspired) artificial neurons 

- everywhere they use a fully connected topology 

- each params is trained 

but it has also been observed depth was not a game changing factor 





## DNN 

The Deep Neural Networks used in Deep Learning show this distinction clearly

- the backbone 

  - is essentially focused on performing automatic feature detection learning 
  
  - makes uses of powerful filters, like Convolutions, relying on parameters sharing hence it's like they slide (e.g. in the case of images) along the full input domain 
  
- the final layer(s) 

  - use(s) the features learned by the core to solve the task 
  
  - makes use of traditional neurons and Dense Layers
  




## Reservoir Computing 

Also in Reservoir Computing this distinction is clear

- the Reservoir 

  - is focused on performing a random high dimensional mapping of the input 
  
  - it is not trainable 
  
- the Readout 

  - is focused on solving the specific task 
  
  - its connections are trainable 





# Underlying Idea

The underlying idea seems to be very similar to the SVM Kernel Trick : as the Readout performs a classification hence essentially finds linear subdivisions in input space, then it should be facilitated by the fact it is high dimensional, as it is the Reservoir output space

The idea seems to be if the Reservoir output space is enough high dimensional, there is no need to train it, hence there is no need to fit this mapping on the data, just focus on training the linear discriminator in this space: this makes training much cheaper and easier

Work in progress







