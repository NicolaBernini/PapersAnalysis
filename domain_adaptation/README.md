
# Overview 

## Introduction 

### What is Unsupervised Domain Adaptation (UDA)

- The Unsupervised Domain Adaptation is a form of Transfer Learning consisting of transferring a capability, for example classification, from the domain where this capability has been acquired to another domain 
- The term unsupervised means that it is assumed no labels are available in the target domain, only data 


### Why UDA

- Currently, Deep Learning Models have been successful a variety of tasks with very high-level performance but these results have been achieved not just thanks to the model itself but also thanks to 
  - a huge amount of data 
  - annotations 

- Supervised Learning Paradigm has a bottleneck related to the availability of labels hence all the techniques that can help to mitigate this issue, including UDA, are considered very useful now 



### Why do we need domain adaptation

- Let's consider a domain is approximate a by a Dataset $D$ so we have 2 domains $D_{1}$ and $D_{2}$ approximated as a set of samples and let's call their data distribution PDF as $P(D_{1})$ and $P(D_{2})$ 
- ML is a data-driven approach hence it is inherently influenced by data, we can think as the NN is a **computation machine** capable of elaborating some input data $x \in X$ to produce output data $y \in Y$ given a certain program $\theta \in \Theta$ so 

$$ f_{NN}(x; \theta) \rightarrow y $$

- Let's also observe the program $\theta$ is very "machine-specific" so it can't run on a different architecture than the original one so when we say $\theta$ we actually mean $f_{NN}(\cdot; \theta)$ 

- In Supervised Learning, this program $\theta$ is learned via the process of training on a certain Dataset $D$ so we can say the NN parameterization $\theta$ depends, among other things like the other aspects of training like the optimizer and its configuration, on this dataset $\theta(D, \cdot)$ hence on the related samples distribution $\theta(P(D), \cdot)$ 

- What happens when a "program" $\theta_{D_{1}}$ runs on a different set of data $D_{2}$ ? 
- This is what happens for example when the trained NN is tested on the Test Set to measure its generalization capability so the capability of working well on data which did not contribute to synthesize its program 

- From a statistical perspective, the point is the 2 datasets have a different distribution so $P(D_{1}) \neq P(D_{2})$ but for the purpose of measuring the generalization on the Test Set, the underlying assumption is the 2 distributions are still reasonably similar to justify the above process so we can formalize this by saying 

$$d(P(D_{1}), P(D_{2})) < d_{th}$$ 

- with 
  - $d(\cdot, \cdot)$ some PDF similarity measure 
  - $d_{th}$ some similarity threshold 

- In the case of domain adaptation, this assumption is does not hold anymore hence it is unreasonable to hope the $\theta_{D_{1}}$ can generalize to $D_{2}$ without some kind of "adaptation" and this is what the domain adaptation consists of 





# Papers about Domain Adaptation 

## [Universal Domain Adaptation through Self Supervision](universal_domain_adaptation_through_self_supervision.md)

![image](https://user-images.githubusercontent.com/6381645/85234560-68433c00-b40e-11ea-9994-ab7a1b2a28f5.png)

---------
