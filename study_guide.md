# ML Interview Study Guide

Machine learning interview questions come in 4 categories

1. algorithms and theory 
2. Programming skills
3. General interest in machine learning
4. company or industry-specific questions

## Questions
1. What is the trade-off between bias and variance?

A model's prediction error can be broken down into bias and variance, and understanding the decomposition of this error is important in avoiding underfitting and overfitting. ```Err(x) = Bias^2 + Variance + Irreducible Error``` 

Bias
: Error introduced from erroneous assumptions of our model. the delta between the average prediction of our model and the correct value we are trying to predict. High bias leads to an oversimplified model (underfitting).

Variance
: The type of error that occurs due to a model's sensitivity. How responsive is the model to changes in the input data. High variance leads to the model learning the noise in the data set (overfitting)

Irreducible Error
: The error that can't be removed by creating good models. A measure of the amount of noise in our data.

Making the model more complex or adding more variables reduces bias but gain some variance. 
