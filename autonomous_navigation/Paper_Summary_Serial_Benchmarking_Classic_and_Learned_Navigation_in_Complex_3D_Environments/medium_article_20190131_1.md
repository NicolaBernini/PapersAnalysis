
# Paper Summary (Serial): Benchmarking Classic and Learned Navigation in Complex 3D Environments

Original Article: [Benchmarking Classic and Learned Navigation in Complex 3D Environments](https://arxiv.org/abs/1901.10915)

## Episode 1  —  Reading through the introduction

### What are the main approaches to autonomous navigation

There are essentially 3 approaches:

- classic ones, based on complex problem modularization in order to solve them with manually engineered solutions and then perform manual integration

- end-to-end learned ones (just providing input and desired output and let the learning system figure out how to solve the loss minimization problem)

- a mix of the two, typically consisting of manually defined modularization and implementing the modules with learning / manual engineering



### What are the challenges for this kind of system

The main challenges are

- achieving robustness: it means the system has to be able to perform well even in presence of noise (Gaussian and Non Gaussian, affecting the system in many ways) and possibly, as the noise grows, the performance should degrade gracefully (i.e. avoiding abrupt degradation as much as possible)

- achieving generalization capability: not only the learned system depend on data but also the manually engineered, in fact the manual engineering is done with respect to some data, which means dataset bias also affects manually engineered system but in a more subtle way. As a result of this issue, the capability of the system to perform well even in presence of data it has never previously “seen” is very desirable property which is also hard to achieve

- achieving scalability: how does the system work when the map becomes 10x bigger? Or the path to navigate becomes 50x longer? Or the number of obstacles in the scene is 30x and they move in a non trivial way? Scalability challenge touches different aspects



### What does this figure show

![Img1](https://cdn-images-1.medium.com/max/800/1*-naGFRhKDuvngvBEiOwUxA.png)

This figure shows the performance of a classic and learned pipeline in 2 relevant scenarios:

- top row represents a complex environment with obstacles, it is shown that manually engineered systems perform better

- bottom row represents a simpler environment but with repetitive patterns, this issue affects the manually engineered system hence the learned system works better



### In last row, where does the manually engineered system fail

It’s the localization module failing, as the repetitive pattern does not provide enough information to perform localization successfully



### Why is the learned system less / not affected then

The learned system uses a different world representation from the manually engineered system one: the latter relies on manually engineered features which are affected by repetitive patterns, the former relies on features which are automatically learned from data.

It means the learned system can “cheat” a little bit performing some overfitting but at the same time it could be a limitation as it could lead to a loss in terms of generalization capability.





### How can the top row failure be classified

I think it is possible to say the learned system fails due to a generalization issue: probably in its training set there were not enough examples to let it understand

- obstacle appearance (so it could have been a perception issue)

- obstacle avoidance (so it could have been a control issue)



### How can the bottom row failure be classified

It’s a robustness issue



### Episode 2 — State of the Art Analysis

To be released by next week


