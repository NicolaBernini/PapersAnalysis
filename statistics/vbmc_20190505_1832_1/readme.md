
# Paper Summary - Variational Bayesian Monte Carlo
​
Original Paper 
​
[Variational Bayesian Monte Carlo](https://arxiv.org/abs/1810.05558?fbclid=IwAR2Irobgi5jW_RVJL4iRyv0QS_WfmgzKk-KmyoeXSZf3X26eFkz8gaTRxk4)
- Published in [NIPS 2018](https://papers.nips.cc/paper/8043-variational-bayesian-monte-carlo)
​
The **goal** is about performing Bayesian Inference hence computing the Model Posterior given a Dataset 
​
Sticking to paper notation we have 
​
- $\mathcal{D}$ : Dataset 
- $x \in \mathcal{X}$ : Model Parametrization 
​
the goal is to compute 
​
1. Model Posterior 
​
$$ P(x | \mathcal{D}) = \frac{P(\mathcal{D} | x) P(X)}{P(\mathcal{D})} $$
​
​
2. Marginal Likelihood or Model Evidence 
​
$$ P(\mathcal{D}) = \int_{\mathcal{X}} P(\mathcal{D} | x) P(x) dx $$
​
​
Of course in practical cases the closed form computation is impossible because of intractable integral hence **approximation methods** need to be used 
​
## Approximation Methods 
​
The cost related to the approximation methods regards the **kind** and **amount of knowledge** that is needed: 
​
- **gradient** is typically a valuable information but not always accessible, like in the case of Black Box Functions 
- **samples** are accessible also in the case of black box functions, however as they have an associated **evaluation cost** the **samples efficiency** of the estimation algorithm is an important aspect 
​
The Variational Inference Framework is based on the of approximating the True Posterior $P(x | \mathcal{D})$ with a simpler Parametric Function $q_{\theta}(x)$ and to fit its params $\theta$ so to make it as simple as possible to the original one 
​
This params fitting problem is defined as a Similarity Distance Minimization problem between the 2 PDFs hence using an appropriate PDF Similarity Function (e.g. KL Divergence)
​
​
​
## Goal 
​
This paper proposes a method working with **Black Box Model Likelihood** (no gradient needed) to perform **Model Posterior Approximation** via **Variational Inference** using 
- Active Sampling strategy, to make it a **data efficient** method 
- Bayesian Quadrature Framework relying on Gaussian Process as a prior to approximate the Likelihood 
​
​
​
​
Appunto 
​
​





​
