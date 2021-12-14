---
layout: distill
title: Interpretable Spatio-Temporal Modeling
description: Identify predictable and interpretable feature subsets from high-dimensional feature space of mixed distribution. 
img: /assets/img/spatio_temporal_modeling/galaxy.jpg
start: 2018
publish: 2018

authors:
  - name: Yong Zhuang
    url: "https://yong-zhuang.github.io"
    affiliations:
      name: UMASS Boston
  - name: David L Small
    affiliations:
      name: Tufts
  - name: Xin Shu
    affiliations:
      name: UMASS Boston
  - name: Kui Yu
    url: "https://sites.google.com/site/yukuiwebsite"
    affiliations:
      name: Hefei University of Technology
  - name: Shafiqul Islam  
    url: "https://engineering.tufts.edu/cee/people/faculty/shafiqul-islam"
    affiliations:
      name: Tufts
  - name: Wei Ding
    url: "https://www.cs.umb.edu/~ding/"
    affiliations:
      name: UMASS Boston

bibliography: hf/hf.bib

# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Objective
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Proposed Model
---
The work on this project has published in ICNSC 2016 and ICBK 2018. Take a look at ["An evaluation of big data analytics in feature selection for long-lead extreme floods forecasting"]({{ 'zhuang2016evaluation/paper.pdf' | prepend: '/assets/pdf/' | relative_url }}) and ["Galaxy: Towards Scalable and Interpretable Explanation on High-Dimensional and Spatio-Temporal Correlated Climate Data"]({{ 'zhuang2018galaxy/paper.pdf' | prepend: '/assets/pdf/' | relative_url }}) for more details.
## Objective
Given a large-scale Spatio-temporal database, effectively and efficiently identifying strongly related features and removing the irrelevant or less important features with respect to a target variable is a critical and challenging issue in many fields. The optimal sub-feature-set that contains all the valuable information is called the Markov Boundary. Unfortunately, the existing feature selection methods often focus on identifying a single Markov Boundary, when real-world data could have many feature subsets that are equally good boundaries. In our work, we studied the existing state-of-the-art streaming feature selection methods. We evaluated them on meteorological data to identify the precursors to heavy precipitation event clusters. We also designed a new multiple-Markov-boundary-based predictive model, Galaxy, for long lead rainfall forecasting.

## Streaming feature selection on large-scale Spatio-temporal database
<img class="float-left w-75" src="{{ 'spatio_temporal_modeling/icnsc2016.jpg' | prepend: '/assets/img/' | relative_url }}"/>
In practical Spatio-temporal applications, transformations and interactions among a small original feature set can lead to a combinatorial increase in feature set size. For example, considering interactions of the nine original meteorological features in 5,328 locations and ten days in a flooding forecasting problem led to a set of over 479,520 potential features. Streaming feature selection has always been a superior technique to interweave the feature generation process with the feature testing process to avoid generating features that are unlikely to be helpful. It continuously updates the subset of predicted features through correlation analysis of newly emerging features, target features, and selected features to remove irrelevant and redundant features and select the most relevant features. [We evaluated four state-of-the-art streaming feature selection methods (Alpha-investing, Online Streaming FeatureSelection (OSFS), Scalable and Accurate Online Approach (SAOLA), and Group SAOLA) on meteorological data sets to identify the precursors to heavy precipitation event clusters]({{ 'zhuang2016evaluation/paper.pdf' | prepend: '/assets/pdf/' | relative_url }}). Through online redundancy analysis, OSFS significantly reduces the learning complexity (only 68 features are selected from 479,520 candidate features while Alpha-investing is 112) and provides us a more accurate precursor feature set with the most potent ability to predict heavy rain events. However, with the effort of online pairwise comparisons and group information, SAOLA and Group SAOLA only select 15 and 8 features, respectively, and the performance of predictive models using the selected feature sets is still comparable.


## Identify multiple Markov boundaries in large-scale Spatio-temporal database
<img class="float-right w-50" src="{{ 'spatio_temporal_modeling/galaxy2.jpg' | prepend: '/assets/img/' | relative_url }}"/>
The ultimate goal of the feature selection method is to identify the feature set most relevant to the target feature, which is called the Markov boundary. In an ideal situation, the joint probability distribution $$P$$ is faithful to $$G$$(the graph of the Bayesian network), there is a unique Markov boundary of the target variable. However, the faithfulness condition almost never holds in real-world data because of hidden variables, hypothesis test errors, and some fake relevance of pure chances, which makes the Markov boundary of the target variable not unique in common situations. Motivated by this, we design a new algorithm,  [Galaxy]({{ 'zhuang2018galaxy/paper.pdf' | prepend: '/assets/pdf/' | relative_url }}), to identify multiple Markov boundaries through equivalent information exploration. We first determine a Markov boundary $$M$$, then try to replace $$A\in M$$ with the potential equivalent feature set $$B$$ explored from the residual features through correlation and performance analysis. We applied Galaxy to an extremely high-dimensional meteorological data set and finally determined 15 Markov boundaries related to heavy rainfall events in the Des Moines River Basin in Iowa, where the smallest size is four and the largest size is 13. Our model identified the cold surges along the coast of Asia as an essential precursor to the surface weather over the United  States, a finding which climate experts later corroborated. 
