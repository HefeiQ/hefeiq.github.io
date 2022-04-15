---
layout: page
title: Sacred Heart
---


**Introduce myself**

My name is Yong Zhuang, and I have received my Ph.D. in Computer Sciencee at the University of Massachusetts Boston. My advisor is Dr. Wei Ding. My research interests broadly include Machine Learning, Big Data Analysis, Feature Selection, Spatio-temporal Data Analysis, and Time Series Prediction. 

Besides research, I worked as a teaching assistant for several courses, such as Artificial Intelligence, Big Data Analysis, and Introduction to Computing. I also worked as an instructor at the student success center, counseling(/ˈkaʊnsəlɪŋ/) disadvantaged students to succeed in their compulsory(/kəmˈpʌlsəri/) courses such as Theory of Computation, Data Structures and Algorithms.

I enjoy teaching and research with the students and colleagues.	

Before studying at UMASS Boston, I worked as a software engineer for 5 years. This job helped me accumulate a wealth of experience in application design, data management, code design, debugging, and testing. It is beneficial for my research work in my Ph.D. study.

**Brief Describe your research**

My research interests broadly include Machine Learning, Big Data Analysis, Feature Selection, Spatio-temporal Data Analysis, Time Series Prediction, and Chaos Theory. (I have published five peer-reviewed full papers in these areas.)

 - **Feature Selection on Big Spatio-temporal Data**: I collaborated with scientists in the Department of Civil and Environmental Engineering at Tufts University to design a new multiple-Markov-boundary-based Feature Selection algorithm, Galaxy(ICBK2018), for long lead extreme precipitation forecasting.

 - **Deep Learning on Big Spatio-temporal Data**: I collaborated with scientists in the School of Criminology and Justice Studies at UMASS Lowell to design a Spatio-temporal recurrent neural network to forecast crime hot spots(ICBK2017).

 - **Time series prediction in chaotic system**: I develop a new recurrent neural network architecture (Error Trajectory Tracing) to track the trajectory of the prediction error through the phase space, and a new training strategy (Horizon Forcing) to expand the prediction horizon of time series(by more than 20%).

 
**Research detail**

 - **Feature Selection on Big Spatio-temporal Data**: 
  * Challenge: Given a large-scale Spatio-temporal data set, effectively and efficiently identifying strongly related features and removing the irrelevant or less important features with respect to a target feature is a critical and challenging issue. 
  
  The optimal sub-feature-set that contains all the valuable information is called the Markov Boundary. Unfortunately, the existing feature selection methods often focus on identifying a single Markov Boundary, when real-world data could have many feature subsets that are equally good boundaries. A single Markov Boundary may not cover all the predictability of the target feature. We expect to identify multiple Markov boundaries containing all the target feature’s predictability and interpretability information for constructing forecasting model to simplify models for more straightforward interpretation and enhanced generalization by reducing over-fitting. Motivated by this, I design a new algorithm, Galaxy, to identify multiple Markov boundaries through equivalent information exploration. <s>(We first determine a Markov boundary M , then try to replace A ∈ M with the potential equivalent feature set B explored from the residual features through correlation and performance analysis.)</s> I applied Galaxy to an extremely high-dimensional climate data set and finally determined 15 Markov boundaries related to heavy rainfall events in the Des Moines River Basin in Iowa. Our model identified the cold surges along the coast of Asia as an essential precursor to the surface weather over the United States(), and this finding was later corroborated by climate experts).

 - **Deep Learning on Big Spatio-temporal Data**: <s>(Some studies have found that)</s> stable hot spots and flow hot spots always exist simultaneously in a specific area, and crime hot spots become more dynamic and unstable as the measurement time and space scale decrease. Therefore, to make specific crime prevention strategies effective and efficient, capturing the temporal evolution of spatial crime patterns has become a critical part of successful crime forecasting models. Deep recurrent neural networks (RNN)<s>(, which have shown impressive performance in several sequence prediction problems, including machine translation, contextual parsing, image captioning, and even video description,)</s> are designed to process sequences and capture the temporal evolution of the objects. In addition, some variants like the Long Short-Term Memory (LSTM) and Gated Recurrent Unit(GRU) can deal with long-term dependencies well. I propose a recurrent neural network to forecast crime hot spots by simulating spatial patterns’ temporal evolution with spatial information embedding. We evaluate the model using call-for-service data provided by the Portland, Oregon Police department (PPB) for five years, <s>(from March 2012 through December 2016)</s>. The experiment results show that our model outperformed several classical machine learning approaches and alternative neural network architectures.

 - **Time series prediction in chaotic system**: <s>The understanding of chaotic systems is challenging not only for theoretical research but also for many critical applications.</s> Chaotic behavior is found in many nonlinear dynamical systems, such as climate dynamics and weather prediction. A reliable solution for these systems must handle their complex space-time dynamics and sensitive dependence on initial conditions. We develop a deep learning framework to push the time horizon at which reliable predictions can be made further into the future by better evaluating the consequences of local errors when modeling nonlinear systems[1]. Our approach observes the future trajectories of initial errors at a time horizon to model the evolution of the loss to that point with two major components: 1) a recurrent architecture (Error Trajectory Tracing) based on the calculation of the Lyapunov exponent, designed to trace the trajectories of predictive errors through phase space, and 2) a training strategy, Horizon Forcing, that pushes the model’s focus out to a predetermined time horizon. We validate our method on three classics, chaotic systems, and four real-world time series prediction tasks with chaotic characteristics, and our approach outperforms the current state-of-the-art methods.
 
 **What is topic of your dissertation?**

 My dissertation mainly focuses on long term prediction on big spatio-temporal data. In terms of the big large-scale Spatio-temporal databases, if we want to discover exciting and previously unknown but potentially useful patterns from data collected over time and space. We should concider temporal and spatial correlations simultaneously. However, with the dimensionality of the time and space measurements increasing, the number of elements potentially contributing to a target sharply grows, making the target's long-term behavior highly complex, chaotic, highly dynamic, and hard to predict. So my study focus on two challenges: 
 
  - big dimensionality: feature selection to identify the most relevant and meaningful features from the original Spatio-temporal feature space in order to improve learning accuracy, reduces the computation time, and facilitates an enhanced understanding for the learning model and data. 
  
  - challenges of forecasting long-term dynamics in nonlinear chaotic systems: sensitive dependencies on initial conditions and exponential error divergence. I proposed a new recurrent architecture(error trajectory tracking) and an training strategy(Horizon Forcing) for prediction in chaotic systems. By better evaluating the consequences of local errors when modeling nonlinear systems, the proposed model can push the time horizon of reliable predictions further into the future.
  