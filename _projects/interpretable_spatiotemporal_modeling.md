---
layout: page
title: Interpretable Spatio-Temporal Modeling
description: Identify the main sub-feature sets with predictive ability and interpretability from the original spatio-temporal space via causal analysis.
img: /assets/img/spatio_temporal_modeling/galaxy.jpg
importance: 2
redirect: 
category: research
---
Given a large-scale Spatio-temporal database, effectively and efficiently identifying strongly related features and removing the irrelevant or less important features with respect to a target variable is a critical and challenging issue in many fields. The optimal sub-feature-set that contains all the valuable information is called the Markov Boundary. Unfortunately, the existing feature selection methods often focus on identifying a single Markov Boundary, when real-world data could have many feature subsets that are equally good boundaries. In our work, we studied the existing state-of-the-art streaming feature selection methods. We evaluated them on meteorological data to identify the precursors to heavy precipitation event clusters. We also designed a new multiple-Markov-boundary-based predictive model, Galaxy, for long lead rainfall forecasting.

##### **Streaming feature selection on large-scale Spatio-temporal database**
<div class="post">
    <div class="profile float-left w-75">
        <img class="img-fluid" src="{{ 'spatio_temporal_modeling/icnsc2016.jpg' | prepend: '/assets/img/' | relative_url }}"/>
    </div>
</div>
In practical Spatio-temporal applications, transformations and interactions among a small original feature set can lead to combinatorial increase in feature set size. For example, considering interactions of the nine original meteorological features in 5,328 locations and ten days in a flooding forecasting problem led to a set of over 479,520 potential features. Streaming feature selection has always been a superior technique to interweave the feature generation process with the feature testing process to avoid generating features that are unlikely to be helpful. It continuously updates the subset of predicted features through correlation analysis of newly emerging features, target features, and selected features to remove irrelevant and redundant features and select the most relevant features. [We evaluated four state-of-the-art streaming feature selection methods (Alpha-investing, Online Streaming FeatureSelection (OSFS), Scalable and Accurate Online Approach (SAOLA), and Group SAOLA) on meteorological data sets to identify the precursors to heavy precipitation event clusters]({{ 'zhuang2016evaluation/paper.pdf' | prepend: '/assets/pdf/' | relative_url }}). Through online redundancy analysis, OSFS significantly reduces the learning complexity (only 68 features are selected from 479,520 candidate features while Alpha-investing is 112) and provides us a more accurate precursor feature set with the most potent ability to predict heavy rain events. However, with the effort of online pairwise comparisons and group information, SAOLA and Group SAOLA only select 15, and 8 features, respectively, and the performance of predictive models using the selected feature sets is still comparable.

##### **Identify multiple Markov boundaries in large-scale Spatio-temporal database**
<div class="post">
    <div class="profile float-right w-50">
        <img class="img-fluid" src="{{ 'spatio_temporal_modeling/galaxy2.jpg' | prepend: '/assets/img/' | relative_url }}"/>
    </div>
</div>
The ultimate goal of the feature selection method is to identify the feature set most relevant to the target feature, which is called the Markov boundary. In an ideal situation, the joint probability distribution $P$ is faithful to $G$(the graph of the Bayesian network), there is a unique Markov boundary of the target variable. However, the faithfulness condition almost never holds in real-world data because of hidden variables, hypothesis test errors, and some fake relevance of pure chances, which makes the Markov boundary of the target variable not unique in common situations. Motivated by this, we design a new algorithm,  [Galaxy]({{ 'zhuang2018galaxy/paper.pdf' | prepend: '/assets/pdf/' | relative_url }}), to identify multiple Markov boundaries through equivalent information exploration. We first determine a Markov boundary $M$, then try to replace $A\in M$ with the potential equivalent feature set $B$ explored from the residual features through correlation and performance analysis. We applied Galaxy to an extremely high-dimensional meteorological data set and finally determined 15 Markov boundaries related to heavy rainfall events in the Des Moines River Basin in Iowa, where the smallest size is four and the largest size is 13. Our model identified the cold surges along the coast of Asia as an essential precursor to the surface weather over the United  States, a finding which was later corroborated by climate experts.