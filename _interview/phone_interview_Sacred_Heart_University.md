---
layout: page
title: Faculty Position
---
["Phone Interview Questions"]({{ 'interview/faculty_phone_interview.pdf' | prepend: '/assets/pdf/' | relative_url }})
### Persional questions

**Are you still interested in the position?**

First of all, I love an academic career. During my Ph.D., I enjoyed teaching and researching with young students and other colleagues. As an educator, I feel very fulfilled when students are satisfied with my courses or help students find jobs/internships. As a researcher, I aspire to conduct research that can change people's daily lives.

In addition, Sacred Heart University has a graduate program that provides the opportunity to conduct research with graduate students. I have intensive experience in Deep learning, Feature selection, and Spatio-temporal data analysis. I want to involve more students in such research fields. 

Moreover, your department is similar to mine in terms of size. I like the friendly working environment, especially not big size, where colleagues can have close relationships even outside the university. And I wish I had the opportunity to contribute to the department. 

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

 - **Time series prediction in chaotic system**: <s>The understanding of chaotic systems is challenging not only for theoretical research but also for many critical applications.</s> Chaotic behavior is found in many nonlinear dynamical systems, such as climate dynamics and weather prediction. A reliable solution for these systems must handle their complex space-time dynamics and sensitive dependence on initial conditions. We develop a deep learning framework to push the time horizon at which reliable predictions can be made further into the future by better evaluating the consequences of local errors when modeling nonlinear systems. Our approach observes the future trajectories of initial errors at a time horizon to model the evolution of the loss to that point with two major components: 1) a recurrent architecture (Error Trajectory Tracing) based on the calculation of the Lyapunov exponent, designed to trace the trajectories of predictive errors through phase space, and 2) a training strategy, Horizon Forcing, that pushes the model’s focus out to a predetermined time horizon. We validate our method on three classics, chaotic systems, and four real-world time series prediction tasks with chaotic characteristics, and our approach outperforms the current state-of-the-art methods.
 
 **What is topic of your dissertation?**

 My dissertation mainly focuses on long term prediction on big spatio-temporal data. In terms of the big large-scale Spatio-temporal databases, if we want to discover previously unknown but potentially useful patterns from data collected over time and space. We should concider temporal and spatial correlations simultaneously. However, with the dimensionality of the time and space measurements increasing, the number of elements potentially contributing to a target sharply grows, making the target's long-term behavior highly complex, chaotic, highly dynamic, and hard to predict. So my study focus on two challenges: 

  - big dimensionality: feature selection to identify the most relevant and meaningful features from the original Spatio-temporal feature space in order to improve learning accuracy, reduces the computation time, and facilitates an enhanced understanding for the learning model and data. 
  
  - forecasting long-term dynamics in nonlinear chaotic systems is challenging with sensitive dependencies on initial conditions and exponential error divergence. I proposed a new recurrent architecture(error trajectory tracking) to better evaluating the consequences of local errors when modeling nonlinear systems. The proposed model can push the time horizon of reliable predictions further into the future.


### Teaching related questions
  **What teaching experience do you have?**

I have served as a teaching assistant for several courses, such as Artificial Intelligence, Big Data Analysis, and Introduction to Computing. 

 - Design semester-long in-class projects.
 - Closely advised students on these projects.
 - Grade students’ homework and projects.
 - Provide several lectures for each course.
 - Hold Q&A sessions through office hours twice a week


I also worked as an instructor at the student success center, counseling(/ˈkaʊnsəlɪŋ/) disadvantaged students to succeed in their compulsory(/kəmˈpʌlsəri/) courses such as Theory of Computation, Data Structures and Algorithms. I offer a 60-minute presentation weekly.

 - Provide practical guidance(/ˈgaɪdn̩s/) and answer specific questions.
 - Previewing upcoming course content, assignments and predicting future challenges.

**What courses would you like to teach?**

I can teach courses at both the undergraduate and graduate levels.  for example,

 - CS 100 INTRO TO INFO TECHNOLOGY 
 - CS 111 INTRO STRUCTURED PROGRAMMING 
 - CS 112 DATA STRUCTURES
 - CS 125 CS EXPLORATIONS 
 - CS 236 ADVANCED SCRIPTING CONCEPTS
 - CS 261 PROGRAMMING FOR THE WEB 
 - CS 311 DATABASE DESIGN
 - CS 312 CS 461 SOFTWARE ENGINEERING
 - CS 341 ANALYSIS OF ALGORITHMS
 - CS 481 INTRODUCTION TO ARTIFICIAL INTELLIGENCE
 - CS 482 APPLIED MACHINE LEARNING
 - CS 501 INTRO TO DATA STRUCTURES
 - CS 504 INTRO TO PROG USING SCRIPTING
 - CS 550 DYNAMIC WEB PAGE DEVELOPMENT
 - CS 551 INTRO OBJECT-ORIENT PRGMG JAVA 
 - CS 553 WEB DESIGN WITH JAVA SCRIPT
 - CS 557 WEB PROGRAMMING WITH ASP 
 - CS 558 ADVANCED ASP.NET 
 - CS 559 C# PROGRAMMING
 - CS 614 THEORY OF COMPUTATION 
 - CS 616 MACHINE LEARNING 
 - CS 617 ARTIFICIAL INTELLIGENCE
 - CS 618 DEEP LEARNINGCS 
 - CS 638 ADV. SCRIPTING WITH PYTHON

I am highly motivated to design new courses based on students’ needs and the department’s needs. such as feature selection, time series analysis.

**How to deal with various(diverse) student backgrounds?**
 I have diverse student population. Some of the students are from college of management and some of the students are part-time that work in the financial industry.
I would choose to provide additional help for less-prepared students. For example, I usually hold extra review sessions to offer them more guidance and equip them of necessary basic knowledge. For those of the students that do not have much time on campus, I will setup the distance learning tools. For example, the online discussion board let them ask question after class. And those settings work well in my course that one of my part time student works for State Street always ask question in the midnight and he got better and better.
In addition, I tend to provide different homeworks, projects and even examples in class to lower the bar of the course and boosts self-confidence.

**what is your strengths and weaknesses in teaching and research**

strengths: like to work with students and colleges, share ideas with them. I like to look for hard problems to solve and where I can learn and develop the most.

weaknesses: non-native speaker, have accent(/ˈækˌsɛnt/) in my english speaking. I like to provide slides and figures to let what I said easy to understand.

**Other questions**
What is the timeline for this searching?

What is the teaching load for new faculty members?

Is the any strategic(/strəˈtiːʤɪkəl/) plan for the department? For example, in 5 years or 10 years.

Is there any special services required for faculty members?





