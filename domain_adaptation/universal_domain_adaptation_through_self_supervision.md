
# Universal Domain Adaptation through Self Supervision

https://arxiv.org/abs/2002.07953

![image](https://user-images.githubusercontent.com/6381645/85234560-68433c00-b40e-11ea-9994-ab7a1b2a28f5.png)

# Universal Domain Adaptation through Self Supervision

[Universal Domain Adaptation through Self Supervision](https://arxiv.org/abs/2002.07953?fbclid=IwAR3ZHDaXuPucHEYxR1_jNmCr5huUJ4fK4q9wbqeNp-MwFid3E7q5-MuWk2I)

# Analysis 

- NN as $Y = f(X)$ with 
  - $X$ : Source Domain 
  - $Y$ : Target Domain 

- In the Training Set we have 
  - $P(X_{train})$ : Source Domain Training Distribution 
  - $P(Y_{train})$ : Target Domain Training Distribution 

- In the Test Set andin Production we have 
  - $P(X_{test})$ : Source Domain Test Distribution 
  - $P(T_{test})$ : Target Domain Test Distribution 

The underlying assumption for the NN to work well in practice is $P(X_{training})$ is very similar to $P(X_{test})$ so that both the training and test instances are taken from the same distribution 
Otherwise we are dealing with a **domain adaptation problem** as the Training Domain has changed with respect to the Test Domain 
Let's use the $\tilde P()$ to identify a changed distribution 


## Types of Domain Adaptation 

### Axis 1 : One step vs Multi steps 

- In a DNN there are multiple layers hence multiple domains, let's say $X_{i} = f_{i}(X_{i-1}) \quad i \in \mathbb{N}^{+}$ so 
  - $f_{i}()$ : the i-th processing layer 
  - $P(X_{i-1})$ : the distribution in input to the i-th layer, with $P(X_{0})$ the input distribution 
  - $P(X_{i})$ : the distribution in output of the i-th layer 
- The PDF divergence certainly affects the input domain $\tilde P(X_{train})$ but then it propagates through the DNN causing a domain shift also in deeper layers $\tilde P(X_{i}) \quad i>0$ 

- The level of permeation of the divergence depends on the **learned features transferability** : the more they are transferable, the less the permeation 
- This is also a key factor to achieve **generalization** 
  - in fact in practice it is possible to see the test set source distribution as divergence with respect to the input distribution $P(X_{0}) \rightarrow \tilde P(X_{0})$ 
  - however a DNN able to generalize is robust against this shift in the sense it is able to absorb it instead of letting it permeate through it up to the final layers causing a visible effect on the output 



### Axis 2 : Divergence Type 

There can be 2 types of divergences 
1. **data distribution** only which is called **homoegeneous domain adaptation** 
- so $\tilde P(X)$ but the dimensionality is preserved so $D(X)$ is the same 

2. involving **dimensionality** which is called **heterogeneous domain adaptation** 
- there is a change in the dimensionality $\tilde D(X)$ which also reflects into the data distribution $\tilde P(X)$ 





# References 

[Deep Domain Adaptation In Computer Vision](https://towardsdatascience.com/deep-domain-adaptation-in-computer-vision-8da398d3167f)






