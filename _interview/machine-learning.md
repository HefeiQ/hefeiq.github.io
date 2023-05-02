---
layout: page
title: machine learning
---
["machine learning questions"]({{ 'interview/Interview_Questions.pdf' | prepend: '/assets/pdf/' | relative_url }})

**Briefly describe the flow of a complete machine learning project.**
 - Formulate it into a mathmatic problem
 - Collect samples
 - Feature preprocessing and feature selection
 - Model training and tuning
 - Determine the direction and idea of ​​model tuning: Common methods such as cross-validation, drawing learning curves, etc. overfitting, underfitting, Error analysis: whether it is a problem of parameters or algorithm selection, whether it is a problem of features or of the data itself...
 - Model fusion: 
 - Model deployment: Engineering is result-oriented, and the effect of the model running online directly determines the success or failure of the model. It not only includes its accuracy, error, etc., but also its running speed (time complexity), resource consumption (space complexity), and whether the stability is acceptable.




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

    We will make a model $$\hat{f}(X)$$ of $$f(X)$$ using linear regression or any other modeling technique. So the expected squared error at a point $x$ is

    $$Err(x)=E[(Y-\hat{f}(x))^2]$$

    The $$Err(x)$$ can be further decomposed as

    $$Err(x)=(E[\hat{f}(x)]-f(x))^2+E[(\hat{f}(x)-E[\hat{f}(x)])^2]+\sigma^2_e \\
      =Bias^2+Variance+Irreducible Error
    $$

    $$Err(x)$$ is the sum of $$Bias^2$$, variance and the irreducible error.

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
 - Data normalization, imput missing values, increase sampls, and add noise
 - Regularization. It involves a cost term for the features involved with the objective function
 - Making a simple model. With lesser variables and parameters, the variance can be reduced 
 - Cross-validation methods like k-folds can also be used
 - If some model parameters are likely to cause overfitting, techniques for regularization like LASSO can be used that penalize these parameters
 - dropout、regularization、batch normalization

**Why normalization?**

 - After normalization, the speed of gradient descent to find the optimal solution is accelerated; 
 - Normalization may improve the accuracy because of distance calculation

**Normalization methods**
 - minmax
 - standand
 - non-linear: log

 [reference](https://www.cnblogs.com/LBSer/p/4440590.html)

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



**[What is Bayes’ Theorem? How is it useful in a machine learning context?](https://seeing-theory.brown.edu/bayesian-inference/index.html)**

Bayes Theorem is a method to determine conditional probabilities – that is, the probability of one event occurring given that another event has already occurred. Because a conditional probability includes additional conditions – in other words, more data – it can contribute to more accurate results.

Say a  bookstore manager has information about his customers’ age and income. He wants to know how book sales are distributed across three age-classes of customers: youth (18-35), middle-aged (35-60), and seniors (60+). 

Let us term our data X. In Bayesian terminology, X is called evidence. We have some hypothesis H, where we have some X that belongs to a certain class C.

Our goal is to determine the conditional probability of our hypothesis H given X, i.e., $$P(H | X)$$.

In simple terms, by determining $$P(H | X)$$, we get the probability of X belonging to class C, given X. X has attributes of age and income – let’s say, for instance, 26 years old with an income of $2000. H is our hypothesis that the customer will buy the book.

Pay close attention to the following four terms:

 - **Evidence** – As discussed earlier, $$P(X)$$ is known as evidence. It is simply the probability that the customer will, in this case, be of age 26, earning $2000.
 
 - **Prior Probability** – $$P(H)$$, known as the prior probability, is the simple probability of our hypothesis – namely, that the customer will buy a book. This probability will not be provided with any extra input based on age and income. Since the calculation is done with lesser information, the result is less accurate.
 
 - **Posterior Probability** – $$P(H | X)$$ is known as the posterior probability. Here, P(H | X) is the probability of the customer buying a book (H) given X (that he is 26 years old and earns $2000). 
 
 - **Likelihood** – $$P(X | H)$$ is the likelihood probability. In this case, given that we know the customer will buy the book, the likelihood probability is the probability that the customer is of age 26 and has an income of $2000.
 
 Given these, Bayes Theorem states:

   $$P(H | X) = \frac{P(X | H) * P(H)}{P(X)}$$


**What’s the difference between probability and likelihood?**

 - Probability refers to the chance that a particular outcome occurs based on the values of parameters in a model.
 - Likelihood refers to how well a sample provides support for particular values of a parameter in a model.

When calculating the probability of some outcome, we assume the parameters in a model are trustworthy.

However, when we calculate likelihood we’re trying to determine if we can trust the parameters in a model based on the sample data that we’ve observed.

**Why is “Naive” Bayes naive?**

Naive Bayes is called naive because it assumes that each input variable is independent. This is a strong assumption and unrealistic for real data; however, the technique is very effective on a large range of complex problems.

**How is a decision tree pruned?**

Pruning is a technique in machine learning that reduces the size of decision trees. It reduces the complexity of the final classifier, and hence improves predictive accuracy by the reduction of overfitting. 

Pruning can occur in:

 - Top-down fashion. It will traverse nodes and trim subtrees starting at the root
 - Bottom-up fashion. It will begin at the leaf nodes

**What is a Random Forest?**

A ‘random forest’ is a supervised machine learning algorithm that is generally used for classification problems. It operates by constructing multiple decision trees during the training phase. The random forest chooses the decision of the majority of the trees as the final decision. 

**How does random forest generate the forest? Additionally, why would we use it over other algorithms such as alogistic regression?**
Random forest generates the forest by essentially bootstrapping your dataset to create many different decision tree functions and then aggregating them together to create a superior model that has a lower variance than the individual decision trees have. Because the bootstrapped samples used to create the individual decision tree models are not truly independent, a random subset of the features from the dataset are used to split nodes for purity. This reduces the correlation between individual trees.

The advantage that Random Forest has over models such as logistic regression is that it can capture non-linear relationships in the data and does not make assumptions about continuity in the feature values that models such as logistic regression make.

**Let's say you have a categorical variable with thousands of distinct values, how would you encode it?**
  - One-hot encoding:
    * pros - two levels numeric encoding, naive
    * cons - given the cardinality, dimensions increase, curse of dimensionlity
  - label encoding:
    * pros - numeric vector given the categories
    * cons - does not add any predictive power, confusion around the interpretability
  - count encoding: replacing categories with their counts computed on the train set. 
    * pros - indicative of the frequency, predictive power
    * cons - sensitive to outliers, may result in collision - encoding two categories as the same value.
  - Target encoding - proportion/avg of Y for this categorical level
    * pros - predictive power, better performance, learning from the labels
    * cons - chances of target leakage if not implemented properly

We apply One-Hot Encoding when:

The categorical feature is not ordinal (like the countries above)
The number of categorical features is less so one-hot encoding can be effectively applied
We apply Label Encoding when:

The categorical feature is ordinal (like Jr. kg, Sr. kg, Primary school, high school)
 The number of categories is quite large as one-hot encoding can lead to high memory consumption
[reference](https://wrosinski.github.io/fe_categorical_encoding/)



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

**What is Principal Component Analysis?**

Principal Component Analysis or PCA is a multivariate statistical technique that is used for analyzing quantitative data. The objective of PCA is to reduce higher dimensional data to lower dimensions, remove noise, and extract crucial information such as features and attributes from large amounts of data.

**What Are Some Methods of Reducing Dimensionality?**

You can reduce dimensionality by combining features with feature engineering, removing collinear features, or using algorithmic dimensionality reduction.



**How would you evaluate a logistic regression model?**
  - Accuracy Score
  - Recall: Recall can be thought of as a measure of a classifiers completeness. A low recall indicates many False Negatives.
  - Precision: Precision can be thought of as a measure of a classifiers exactness. A low precision can also indicate a large number of False Positives.
  - F1 Score, if you are dealing with a imbalanced dataset this is a must. If you are looking to select a model that is balanced between precision and recall F measure should be used.

**What’s the “kernel trick” and how is it useful?**

Kernel trick allows the inner product of mapping function instead of the data points. The trick is to identify the kernel functions which can be represented in place of the inner product of mapping functions. Kernel functions allow easy computation. In essence, what the kernel trick does for us is to offer a more efficient and less expensive way to transform data into higher dimensions.



**Explain the difference between L1 and L2 regularization.**

 - L1 regularization penalizes the sum of absolute values of the weights, whereas L2 regularization penalizes the sum of squares of the weights. 
 - The L1 regularization solution is sparse. The L2 regularization solution is non-sparse.
 - L2 regularization doesn’t perform feature selection, since weights are only reduced to values near 0 instead of 0. L1 regularization has built-in feature selection.
 - L1 regularization is robust to outliers, L2 regularization is not. 
 - L1 is a Laplace distribution and L2 is a Gaussian distribution.


**What’s a Fourier transform?**

The Fourier transform is a mathematical function that decomposes a waveform, which is a function of time, into the frequencies that make it up. The result produced by the Fourier transform is a complex valued function of frequency. The absolute value of the Fourier transform represents the frequency value present in the original function and its complex argument represents the phase offset of the basic sinusoidal in that frequency.

**Q9: What’s your favorite algorithm, and can you explain it to me in less than a minute?**




**Q13: What is deep learning, and how does it contrast with other machine learning algorithms?**

**Q14: What’s the difference between a generative and discriminative model?**
Core Idea: Discriminative models draw boundaries in the data space, while generative models try to model how data is placed throughout the space. A generative model focuses on explaining how the data was generated, while a discriminative model focuses on predicting the labels of the data.

Mathematical Intuition: In mathematical terms, a discriminative machine learning trains a model which is done by learning parameters that maximize the conditional probability P(Y|X), while on the other hand, a generative model learns parameters by maximizing the joint probability of P(X, Y).

Outliers: Generative models have more impact on outliers than discriminative models.

Computational Cost: Discriminative models are computationally cheap as compared to generative models.

generative models:
 - Naive Bayes, Hidden Markov Models, Gaussian Mixture Models, Document Topic Generation (LDA), Restricted Boltzmann Machines

discriminative models:
 - K-Nearest Neighbors, SVM, Decision Trees, Perceptrons, Linear Discriminant Analysis (LDA), Linear Regression, Traditional Neural Networks, Logistic Regression, Boosting, Conditional Random Fields

[reference](https://www.analyticsvidhya.com/blog/2021/07/deep-understanding-of-discriminative-and-generative-models-in-machine-learning/#:~:text=Discriminative%20models%20draw%20boundaries%20in,the%20labels%20of%20the%20data.)



**What cross-validation technique would you use on a time series dataset?**

With time series data, particular care must be taken in splitting the data in order to prevent data leakage. In order to accurately simulate the “real world forecasting environment, in which we stand in the present and forecast the future” (Tashman 2000), the forecaster must withhold all data about events that occur chronologically after the events used for fitting the model. So, rather than use k-fold cross-validation, for time series data we utilize hold-out cross-validation where a subset of the data (split temporally) is reserved for validating the model performance. For example, see following figure where the test set data comes chronologically after the training set. Similarly, the validation set comes chronologically after the training subset.
<img class="float-left" src="{{ 'interview/nested_cv.png' | prepend: '/assets/img/' | relative_url }}"/>
<img class="float-left" src="{{ 'interview/summary_nested_cv.png' | prepend: '/assets/img/' | relative_url }}"/>


**What is bagging?**

Bagging, also known as bootstrap aggregation, is the ensemble learning method that is commonly used to reduce variance within a noisy dataset. In bagging, a random sample of data in a training set is selected with replacement—meaning that the individual data points can be chosen more than once. After several data samples are generated, these weak models are then trained independently, and depending on the type of task—regression or classification, for example—the average or majority of those predictions yield a more accurate estimate. 

As a note, the random forest algorithm is considered an extension of the bagging method, using both bagging and feature randomness to create an uncorrelated forest of decision trees.

**Bagging vs. boosting**

Bagging and boosting are two main types of ensemble learning methods. As highlighted in this study (PDF, 248 KB) (link resides outside IBM), the main difference between these learning methods is the way in which they are trained. In bagging, weak learners are trained in parallel, but in boosting, they learn sequentially. This means that a series of models are constructed and with each new model iteration, the weights of the misclassified data in the previous model are increased. This redistribution of weights helps the algorithm identify the parameters that it needs to focus on to improve its performance. AdaBoost, which stands for “adaptative boosting algorithm,” is one of the most popular boosting algorithms as it was one of the first of its kind. Other types of boosting algorithms include XGBoost, GradientBoost, and BrownBoost.

Another difference in which bagging and boosting differ are the scenarios in which they are used. For example, bagging methods are typically used on weak learners which exhibit high variance and low bias, whereas boosting methods are leveraged when low variance and high bias is observed.

**What does S (stochastic) in SGD stand for?**
- Optimization algorithms that use the entire training set are called batch or deterministic gradient algorithms because all samples are processed simultaneously in one large batch.
- Optimization algorithms that use only a single sample at a time are sometimes called stochastic or online algorithms.
- Most algorithms for deep learning fall somewhere in between, using more than one rather than all training samples. They are now commonly referred to simply as stochastic methods.

**LSTM structure derivation, why is it better than RNN?**

Derive the changes of forget gate, input gate, cell state, hidden information, etc.; because LSTM has in and out and the current cell informaton is superimposed after being controlled by the input gate, RNN is multiplication, so LSTM can prevent the gradient from vanishing or exploding.

**Gradients vanishing and exploding**
 - Gradient clipping, regularization: WGAN
 - relu、leakrelu、elu
 - batchnorm
 - residual connection
 - LSTM

**covariance and correlation**

covariance(A, C) cannot compare with covariance(B, C) because of the different ranges of A and B Correlation is the standard covariance.
[reference](https://www.zhihu.com/question/20852004)