---
layout: page
title: machine learning
---
### Algorithms / Theory

**What’s the trade-off between bias and variance?**

In statistics and machine learning, the bias–variance tradeoff is the property of a model that the variance of the parameter estimated across samples can be reduced by increasing the bias in the estimated parameters. The bias–variance dilemma or bias–variance problem is the conflict in trying to simultaneously minimize these two sources of error that prevent supervised learning algorithms from generalizing beyond their training set:

  * What is bias?    
    Bias is the difference between the average prediction of our model and the correct value which we are trying to predict. Model with high bias pays very little attention to the training data and oversimplifies the model. It always leads to high error on training and test data (underfitting).  
    
  * What is variance?    
    Variance is the variability of model prediction for a given data point or a value which tells us spread of our data. Model with high variance pays a lot of attention to training data and does not generalize on the data which it hasn’t seen before. As a result, such models perform very well on training data but has high error rates on test data (overfitting).   
    
  * Mathematically
  
    Let the variable we are trying to predict as Y and other covariates as X. We assume there is a relationship between the two such that

    $$Y=f(X) + e$$

    Where $e$ is the error term and it’s normally distributed with a mean of $0$.

    We will make a model $\hat{f}(X)$ of $f(X)$ using linear regression or any other modeling technique. So the expected squared error at a point $x$ is

    $$Err(x)=E[(Y-\hat{f}(x))^2]$$

    The $Err(x)$ can be further decomposed as

    $$Err(x)=(E[\hat{f}(x)]-f(x))^2+E[(\hat{f}(x)-E[\hat{f}(x)])^2]+\sigma^2_e \\
      =Bias^2+Variance+Irreducible Error
    $$

    $Err(x)$ is the sum of $Bias^2$, variance and the irreducible error.

    Irreducible error is the error that can’t be reduced by creating good models. It is a measure of the amount of noise in our data. Here it is important to understand that no matter how good we make our model, our data will have certain amount of noise or irreducible error that can not be removed.

The bias–variance decomposition is a way of analyzing a learning algorithm's expected generalization error with respect to a particular problem as a sum of three terms, the bias, variance, and a quantity called the irreducible error, resulting from noise in the problem itself.

**What is the difference between supervised and unsupervised machine learning?**

 - **Supervised Learning**
 In supervised machine learning, a model makes predictions or decisions based on past or labeled data. Labeled data refers to sets of data that are given tags or labels, and thus made more meaningful.

 - **Unsupervised Learning**
 In unsupervised learning, we don't have labeled data. A model can identify patterns, anomalies, and relationships in the input data.

**What is Overfitting, and How Can You Avoid It?** 

The Overfitting is a situation that occurs when a model learns the training set too well, taking up random fluctuations in the training data as concepts. These impact the model’s ability to generalize and don’t apply to new data. 

When a model is given the training data, it shows 100 percent accuracy—technically a slight loss. But, when we use the test data, there may be an error and low efficiency. This condition is known as overfitting.

There are multiple ways of avoiding overfitting, such as:

 - Regularization. It involves a cost term for the features involved with the objective function
 - Making a simple model. With lesser variables and parameters, the variance can be reduced 
 - Cross-validation methods like k-folds can also be used
 - If some model parameters are likely to cause overfitting, techniques for regularization like LASSO can be used that penalize these parameters

**How Do You Handle Missing or Corrupted Data in a Dataset?**

One of the easiest ways to handle missing or corrupted data is to drop those rows or columns or replace them entirely with some other value.

There are two useful methods in Pandas:

 - IsNull() and dropna() will help to find the columns/rows with missing data and drop them
 - Fillna() will replace the wrong values with a placeholder value

**How Can You Choose a Classifier Based on a Training Set Data Size?**
When the training set is small, a model that has a right bias and low variance seems to work better because they are less likely to overfit. 

For example, Naive Bayes works best when the training set is large. Models with low bias and high variance tend to perform better as they work fine with complex relationships.

**Explain the Confusion Matrix with Respect to Machine Learning Algorithms.**

|| Actual:Positive      | Actual:Negative ||
|:---  | :---        |  :--- |:---|
|Predicted:Positive| True Positive (TP)  | False Positive (FP) (Type I) | Positive Predictive Value(PPV), Precision $$\frac{TP}{TP+FP}$$
|Predicted:Negative| False Negative (FN) (Type II) | True Negative (TN)||
||True Positive Rate(TPR), Recall, Sensitivity $$\frac{TP}{TP+FN}$$|False Positive Rate(FPR) $$\frac{FP}{FP+TN}$$||

For a model to be accurate, the values across the diagonals should be high. The total sum of all the values in the matrix equals the total observations in the test data set. 

The F1-score combines the precision and recall of a classifier into a single metric by taking their harmonic mean.

$$F1-score = \frac{2(precision * recall)}{precision+recall}$$

 - precision:  A low precision can also indicate a large number of False Positives(Type I).
 - recall: A low recall indicates many False Negatives(Type II).
 
For any system to be able to achieve maximum Precision (no false positive) and maximum Recall (no false negative) there needs to be an absence of type I and II errors.

**Explain how a ROC curve works.**

An ROC curve (receiver operating characteristic curve) is a graph showing the performance of a classification model at all classification thresholds. This curve plots two parameters:

 - True Positive Rate
 - False Positive Rate
An ROC curve plots TPR vs. FPR at different classification thresholds. Lowering the classification threshold classifies more items as positive, thus increasing both False Positives and True Positives. The following figure shows a typical ROC curve.

AUC stands for "Area under the ROC Curve." That is, AUC measures the entire two-dimensional area underneath the entire ROC curve (think integral calculus) from (0,0) to (1,1). 

**How is KNN different from k-means clustering?**

| K-means      | KNN    |
| :---        |  :--- |
| K-Means is unsupervised      | KNN is supervised in nature   |
| K-Means is a clustering algorithm | KNN is a classification algorithm |
| The points in each cluster are similar to each other, and each cluster is different from its neighboring clusters | It classifies an unlabeled observation based on its K (can be any number) surrounding neighbors |



**What is Bayes’ Theorem? How is it useful in a machine learning context?**

Bayes Theorem is a method to determine conditional probabilities – that is, the probability of one event occurring given that another event has already occurred. Because a conditional probability includes additional conditions – in other words, more data – it can contribute to more accurate results.

Say a  bookstore manager has information about his customers’ age and income. He wants to know how book sales are distributed across three age-classes of customers: youth (18-35), middle-aged (35-60), and seniors (60+). 

Let us term our data X. In Bayesian terminology, X is called evidence. We have some hypothesis H, where we have some X that belongs to a certain class C.

Our goal is to determine the conditional probability of our hypothesis H given X, i.e., P(H | X).

In simple terms, by determining P(H | X), we get the probability of X belonging to class C, given X. X has attributes of age and income – let’s say, for instance, 26 years old with an income of $2000. H is our hypothesis that the customer will buy the book.

Pay close attention to the following four terms:

 - **Evidence** – As discussed earlier, P(X) is known as evidence. It is simply the probability that the customer will, in this case, be of age 26, earning $2000.
 
 - **Prior Probability** – P(H), known as the prior probability, is the simple probability of our hypothesis – namely, that the customer will buy a book. This probability will not be provided with any extra input based on age and income. Since the calculation is done with lesser information, the result is less accurate.
 
 - **Posterior Probability** – P(H | X) is known as the posterior probability. Here, P(H | X) is the probability of the customer buying a book (H) given X (that he is 26 years old and earns $2000). 
 
 - **Likelihood** – P(X | H) is the likelihood probability. In this case, given that we know the customer will buy the book, the likelihood probability is the probability that the customer is of age 26 and has an income of $2000.
 
 Given these, Bayes Theorem states:

   $$P(H | X) = \frac{P(X | H) * P(H)}{P(X)}$$

**Why is “Naive” Bayes naive?**

Naive Bayes is called naive because it assumes that each input variable is independent. This is a strong assumption and unrealistic for real data; however, the technique is very effective on a large range of complex problems.

**How is a decision tree pruned?**

Pruning is a technique in machine learning that reduces the size of decision trees. It reduces the complexity of the final classifier, and hence improves predictive accuracy by the reduction of overfitting. 

Pruning can occur in:

 - Top-down fashion. It will traverse nodes and trim subtrees starting at the root
 - Bottom-up fashion. It will begin at the leaf nodes

**Which is more important to you? Model accuracy, or model performance?**
Well, you must know that model accuracy is only a subset of model performance. The accuracy of the model and performance of the model are directly proportional and hence better the performance of the model, more accurate are the predictions.



**How would you handle an imbalanced dataset?**
  - 1. Choose Proper Evaluation Metric
  F1 score keeps the balance between precision and recall and improves the score only if the classifier identifies more of a certain class correctly.

  - 2. Resampling (Oversampling and Undersampling)

  - 3. SMOTE
  Synthetic Minority Oversampling Technique or SMOTE is another technique to oversample the minority class. Simply adding duplicate records of minority class often don’t add any new information to the model. In SMOTE new instances are synthesized from the existing data. If we explain it in simple words, SMOTE looks into minority class instances and use k nearest neighbor to select a random nearest neighbor, and a synthetic instance is created randomly in feature space.

  - 4. BalancedBaggingClassifier
  When we try to use a usual classifier to classify an imbalanced dataset, the model favors the majority class due to its larger volume presence. A BalancedBaggingClassifier is the same as a sklearn classifier but with additional balancing. It includes an additional step to balance the training set at the time of fit for a given sampler. This classifier takes two special parameters “sampling_strategy” and “replacement”. The sampling_strategy decides the type of resampling required (e.g. ‘majority’ – resample only the majority class, ‘all’ – resample all classes, etc) and replacement decides whether it is going to be a sample with replacement or not.

  - 5. Threshold moving

**When should you use classification over regression?**

Classification is about identifying group membership while regression technique involves predicting a response. Both techniques are related to prediction, where classification predicts the belonging to a class whereas regression predicts the value from a continuous set. Classification technique is preferred over regression when the results of the model need to return the belongingness of data points in a dataset to specific explicit categories. (For instance, when you want to find out whether a name is male or female instead of just finding it how correlated they are with male and female names.

**Name an example where ensemble techniques might be useful.**

Ensemble Technique is a machine learning method or technique that combines various base models in order to produce one optimal and predictive model. reduce overfitting and more robust

A good example of how ensemble methods are commonly used to solve data science problems is the random forest algorithm (having multiple CART models). It performs better compared to individual CART model by classifying a new object where each tree gives “votes” for that class and the forest chooses the classification having the most votes (over all the trees in the forest). In case of regression, it takes the average of outputs of different trees.

**How do you ensure you’re not overfitting with a model?**
  - 1- Keep the model simpler: remove some of the noise in the training data.
  - 2- Use cross-validation techniques such as k-folds cross-validation.
  - 3- Use regularization techniques such as LASSO

**What evaluation approaches would you work to gauge the effectiveness of a machine learning model?**

Use the kernel function to ensure that there is no data in the high-dimensional space to calculate the coordinates of the point, and the inner product in the space can be calculated. Many algorithms can express such an inner product form, using kernel energy to ensure that low-dimensional data is calculated in a high-dimensional space.

**How would you evaluate a logistic regression model?**
  - Accuracy Score
  - Recall: Recall can be thought of as a measure of a classifiers completeness. A low recall indicates many False Negatives.
  - Precision: Precision can be thought of as a measure of a classifiers exactness. A low precision can also indicate a large number of False Positives.
  - F1 Score, if you are dealing with a imbalanced dataset this is a must. If you are looking to select a model that is balanced between precision and recall F measure should be used.

**What’s the “kernel trick” and how is it useful?**

Kernel trick allows the inner product of mapping function instead of the data points. The trick is to identify the kernel functions which can be represented in place of the inner product of mapping functions. Kernel functions allow easy computation. In essence, what the kernel trick does for us is to offer a more efficient and less expensive way to transform data into higher dimensions.



**Q8: Explain the difference between L1 and L2 regularization.**

**Q9: What’s your favorite algorithm, and can you explain it to me in less than a minute?**

**Q10: What’s the difference between Type I and Type II error?**

**Q11: What’s a Fourier transform?**

**Q12: What’s the difference between probability and likelihood?**

**Q13: What is deep learning, and how does it contrast with other machine learning algorithms?**

**Q14: What’s the difference between a generative and discriminative model?**

**Q15- What cross-validation technique would you use on a time series dataset?**