
# Machine Learning of Sets 

Original Post: 

http://akosiorek.github.io/ml/2020/08/12/machine_learning_of_sets.html



---------



<table>
<tbody>
<tr>
<td>Original</td>
<td>Comments</td>
</tr>
<tr>
<td>
<img src="https://user-images.githubusercontent.com/6381645/90321544-0228f000-df4b-11ea-85a6-3a3691ae0d54.png"> <br/> 
<img src="https://user-images.githubusercontent.com/6381645/90321597-7fecfb80-df4b-11ea-8511-db3f5f61146e.png">
</td>
<td>
- The NNs try to learn the correlation between $X$ and $Y$ and this is why the IID Assumption of the $x$ and $y$ samples taken from the related distributions is so important for the learning performance
</td>
</tr>
</tbody>
</table>
<!-- DivTable.com -->


-------

AK 

> A common constraint in image-related problems is translation equivariance1—the output of the algorithm should shift with any shifts applied to the image (you can read more about equvariances in this excellent blog post). 

- The blog post explaining Translation Equivariance is this one from Ed Wagstaff & Fabian Fuchs and it is really good

https://fabianfuchsml.github.io/equivariance1of2/

especially the MP4 they used to explain which you find here 

http://edwag.github.io/video/translation_equivariance.mp4

- Anyway it is actually application specific: if you wanted to do detection then you need translation equivariance, while if you wanted to do classification you need translation invariance. But here I am a bit pedantic. 

