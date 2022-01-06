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

2. What is the difference between supervised and unsupervised ML?

Supervised
: Requires labeled training data

Unsupervised
: Does not require labeled training data, attempting to find latent connections between input data

3. How is KNN different from k-means clustering?

KNN
: K-Nearest Neighbors is a *supervised* classification algorithm. 

K-Means
: Unsupervised clustering algorithm. Learns the mean of the distance between the points iteratively. 

4. Explain how a ROC curve works

ROC
: Reciever operating characteristic. A graphical way to show the difference between true positive/false positive rate at various thresholds. Traditionally we are interested in the area under the curve (AUC). A performance measurement for classification problems at various threshold settings. The AUC represents the degree of separability between classes. Higher is usually better. ROC curves can be misleading in highly imbalanced classification scenarios. If this is the case you might be better using a PR curve

5. Define precision and recall

Recall
: AKA true positive rate. The amount of positives your model claims compared to the actual number of positives. How many relevant items are retrieved

Precision
: A measure of the amount of accurate positives your model claims compared to the numberof positives your model claims. How many retrieved items are relevant 

 How many relevant items are retrieved How many relevant items are retrieved How many relevant items are retrieved How many relevant items are retrieved How many relevant items are retrieved How many relevant items are retrieved

6. What is Bayes' Theorem?

Bayes' Theorem
: A way to describe the probability of an event based on prior knowledge of conditions that are related to that event. Leads the the Naive Bayes' Classifier 

P(C|x) = (P(x|C)*P(C)) / P(x)

- P(C|x) = the posterior probability (revised probability based on the consideration of new information). What is the probability of class C given x (features)
- P(C) = the prior probability of a class (the probability of an event before new data is collected)
- P(x|C) = The likelihood. The probability of seeing this predictor given the class. 
- P(X) the prior probability of a predictor. 

Naive Bayes' will assign 0 probability to categorical values not seen in the test data set. The probability estimates should not be taken too seriously. Based on the assumption of independent predictors, which almost never happens in real life. But it is very fast and can be very accurate. 'Naive' comes from the assumption that features are completely indepdenent. If you like pickles and ice cream you probably wouldn't like pickle ice cream.

7. Explain the difference between L1 and L2 regularization

regularization
: A method to reduce overfitting. As the model complexity increases a larger penalty is applied to themodel. 

L1 Regularization
: Lasso regression adds the absolute value of magnitude of coefficient as a penalty term

L2 Regularization
: Ridge regression adds the squared magnitude of coefficient

Lasso (L1) shrinks the important feature's coefficient to zero (feature selection). Ridge regression can work well with multicolinearity. 

8. What is your favorite algorithm?

Meta-algorithms (ensemble learning)

Bagging
: Training multiple models (weak learnings) indepdently and combining them later. results in a final model that is stronger than the individual weak learners. Reduces variance

Boosting
: Trains multiple weak learners sequentially, each additional model aims to improve upon the errors of the previous model. Reduces bias. 

Stacking
: Using a meta learning to combine the results of the base models

9. What is the difference between Type I and Type II errors?

Type I
: False positive, telling a man he is pregnant

Type II
: False negative, telling a pregnant woman she isn't pregnant

10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. 10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. 10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. 10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. 10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. 10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. 10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. 10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. 10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. 10. What is a fourier transform?

A way to decompose generic functions into a superposition of symmetric functions

11. What is the difference between probability and likelihood?

Probability
: finding the chance of something given a sample distribution of the data

Likelihood
: Finding the best distribution for the data based on what we have observed

12. What is the difference between a generative and a discriminative model?

Generative
: Building a model of each class and then identifying which model most accurately describes the input sample

Discriminative
: Attempts to create a decision boundary between classes and then seeing which side of the boundary the sample lies on. 

13. What cross-validation technique would you use on a time series dataset?

Time series data is not randomly distributed, it is inherently ordered by time. Patternsmay emerge in later periods that don't exist in earlier periods. In this case forward chaining is a good way to deal with this. Train on earlier sets and test on later sets. 

14. What is an F1 score?

The F1 score is the weighted average of the precision and recall of a model. 1 is best 0 is worst. Used in classification. 

15. How would you handle an imbalanced dataset?
	
	1. Collect more data to try and even the imbalances
	2. Resample 
	3. Try a different algorithm
	4. Synthetic techniques such as SMOTE

16. How do you ensure that you are not overfitting with a model?

	1. Simplify the model and reduce variance
	2. Use cross-validation techniques 
	3. Use regularization techniques such as lasso 

17. How do you handle missing or corrupted data in a dataset?

You can either drop those rows or replace them with another value (average, mean, etc). You can also focus on using models that allow you to have null values as not having a value is a piece of information. 

18. What are the data types supported by json?

strings, numbers, objects, arrays, booleans, and null

19. What is the difference between one-hot encoding and label encoding?

Label encoding is converting labels/words into a numeric form. One-hot encoding is representing categorical variables as a binary vector. One-hot encoding increases the dimensionality of the data. 

20. Standard deviation vs variance

standard deviation (sigma) = variance^2 (sigma^2)

21. For both gradient descent and stochastic gradient descent you are updating a set of parameters in an iterative manner to minimize an error function. Gradient descent relies on using all the samples to do a single update of the parameters, SGD uses only a single sample or a minibatch

22. What is principal component analysis (pca)?

A technique to reduce the dimensionality of input data. The principal components are the eigenvectors of the covariance matrix. 

23. What is the difference between regularization and normalization?

Normalization impacts the input data. Regularization impacts the predictive function

24. What is the difference between normalization and standardization?

Normalization scales values to [0, 1] while standardization scales values to have a mean of 0 and a standard deviation of 1

25. What are the most common distributions?

Bernoulli
: A special case of a binomial distribution with 1 trial, pass or fail an exam etc

Uniform
: A constant probability, rolling a single dice (fixed # of outcomes)

Binomial 
: Only 2 possible outcomes

Poisson 
: predict the probability of certain events when you know how often an event has occurred

Exponential 
: the amount of time until a specific event occurs  

## Leetcode Tips

1. If input array is sorted:
	- Binary Search
	- Two Pointers
2. If asked for all permutations/subsets
	- Backtracking
3. If given a tree
	- Depth first search
	- Breadth first search
4. If given a graph
	- Depth first search
	- Breadth first search
5. If given a linked list
	- Two pointers
6. If recursion if banned
	- Stack
7. If must solve in place
	- Swap corresponding values
	- Store one or more different values in the same pointer
8. If asked for maximum/minumum subarray/subset/options
	- Dynamic programming
9. If asked for top/least K items 
	- Heap
10. If asked for common strings
	- Map
	- Trie
11. Else
	- Map/set for O(1) time & O(n) space)
	- Sort input for O(nlogn) time and O(1) space

