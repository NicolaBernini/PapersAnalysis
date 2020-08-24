
# Overview 

Challenges related to Testing in the Deep Learning world 

- Coding Deep Neural Networks is currently often perceived by ML Engineers / Scientists as a much less error-prone activity than traditional SW Engineering 
- So no proper bug hunting strategy is typically developed, sometimes there is no strategy at all 
- This might be related to the fact a bug in ML code has a subtle behavior: it could stay unnoticed for a long time as it might not produce clear signals of its presence like crashing, broken interface, ... in fact, it could silently corrupt the data and the researcher could interpret this as the result of an issue not lying at the code level, like overfitting, class imbalances, ... 
- Certainly, ML code regards a narrower scope than code in other domains and the powerful ML and DL Frameworks positively contribute to reducing the lines of code that researcher / engineer need to write (moving a lot of complexity under the framework hood, so it is addressed by the framework developers once instead of each researcher individually) still these lines of code could be bugged: for example, think about the effect of a bug in the loss function or in the data pre-processing or post-processing pipeline 












