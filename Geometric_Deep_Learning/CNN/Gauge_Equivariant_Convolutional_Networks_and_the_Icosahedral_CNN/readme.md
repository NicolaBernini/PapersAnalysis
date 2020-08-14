
# Paper Summary - Gauge Equivariant Convolutional Networks and the Icosahedral CNN 

Original Paper: [Gauge Equivariant Convolutional Networks and the Icosahedral CNN](https://arxiv.org/abs/1902.04615)

Note 

- As there is some math pleas activate a Browser Side Tex Rendering Plugin like [Tex all the things](https://chrome.google.com/webstore/detail/tex-all-the-things/cbimabofgmfdkicghcadidpemeenbffn) 

# Intro 

Main Elements 

- **Convolutional Filter** is a Filter mapping from a Domain to a Co-domain 
  - $f : \mathcal{D} \rightarrow \mathcal{C}$
  - In CNN context, it maps a feature map into another feature map 

- **Equivariance** is a property regarding both a filter and its domain of application: 
  - when a transformation is applied to the filter domain and it fully reflects on the filter output then the filter is called **equivariant** with respect to that transformation 
    - $f(g(x)) = g(f(x))$ or equivalently 
    - $g^{-1}(f(g(x))) = f(x)$ (we will use this specific definition later )
  - if the transformation gets fully absorbed by the filter, so that there is no trace of its application in the filter output, then the filter is called **invariant** with respect to that transformation 
    - $f(g(x)) = f(x)$

- **Symmetries** is a set of transformations related to a specific space only (so it does not depend on any filter) which map the space in itself without altering its structure 

- The underlying idea between the Classical CNN Layer acting on an Image or generic Planar Feature Map, is to be able to **slide** it over the plane or equivalently to **slide** the plane under it hence more formally to use one of the **plane symmetries** to transform the plane in itself before processing it again and again with Convolutional Filter 
  - Generalizing this procedure on a generic space, we would like 
  1. something the works the same way hence transforming the space in itself for continuous processing 
  2. the Convolutional Filter result should not depend on the specific position (this is typically called **parameters sharing** and it makes CNN Processing **position independent**)


- In terms of space generalization, let's consider a **Manifold** $M$ which is a space which is locally homeomorphic to an Euclidean Space 
  - Hence given a point $p \in M$ we have a local tangent space $T_{p}M$ where we can define an **invertible linear mapping** between this Tangent Space and the Eucliden 


- Unfortunately we can not simply apply the manifold equivalent for the plane shift (transformation member of plane symmetries set) because a generic manifold does not provide any guarantee to possess any global symmetry 
  - This means with a manifold we can not approach the problem at the global level hence we need to work at a local level, hence considering a point $p$ its neighborhood is a Tangent Space $T_{p}M$ which has the beautiful property of being homeomorphic to the Euclidean Space 



- Let's then introduce the **Gauge** which is a **Position Dependent Invertible Local Linear Mapping** between the Manifold Tangent Space $T_{p}M$ and the Euclidean Space $\mathbb{R}^{d}$  
  - $w_{p} : \mathbb{R}^{d} \rightarrow T_{p}M$ and $\exists w_{p}^{-1}$

- As a result of this, a Gauge also defines a Local Reference Frame in $T_{p}M$ (mapping the Euclidean Reference Frame) 
  - In fact if $\{e_{i}\}$ is basis for $\mathbb{R}^{d}$ then $\{w_{p}(e_{i})\}$ is the corresponding Gauge basis for $T_{p}M$


- A **Gauge Transformation** is a **Position Dependent Invertible Change of the Local Frame** 
  - Mathematically if $w_{p}$ is a Gauge, then $g_{p} \in GL(d, \mathbb{R})$ is a Gauge Transformation so that $w_{p} \rightarrow w_{p}g_{p}$
  - With $GL(d, \mathbb{R})$ group of invertible $d \times d$ matrix 

- In order for the **filter sliding** to work properly we need to the Filter to be equivariant with respect to gauge transformation 
  - Let's call $v_{p}$ the filter output feature map described with respect to the Gauge $w_{p}$
  - In order for the filter to be equivariant to the Gauge Transformation $g_{p}$ according to the above definition we need 
  
$$ (w_{p}g_{p})(g_{p}^{-1}v_{p}) = v_{p} $$


- The underlying idea is hence to build a filter with this property, depending on the specific manifold it has to process 

Work in progress 









