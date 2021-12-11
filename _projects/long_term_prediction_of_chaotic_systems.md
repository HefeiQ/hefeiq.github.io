---
layout: distill
title: Long-term prediction of chaotic systems
description: using new deep architectures to learn the state evolution of a variety of chaotic dynamical systems and significantly extend the prediction time.
img: /assets/img/chaos/hf.jpg
importance: 2
redirect:   
category: research

start: 2019
publish: 

authors:
  - name: Yong Zhuang
    url: "https://yong-zhuang.github.io"
    affiliations:
      name: UMASS Boston
  - name: Matthew Almeida
    url: "https://matthewalmeida.github.io/"
    affiliations:
      name: UMASS Boston
  - name: Wei Ding
    url: "https://www.cs.umb.edu/~ding/"
    affiliations:
      name: UMASS Boston
  - name: Patrick D Flynn
    affiliations:
      name: UMASS Boston
  - name: Shafiqul Islam  
    url: "https://engineering.tufts.edu/cee/people/faculty/shafiqul-islam"
    affiliations:
      name: Tufts
  - name: Ping Chen  
    url: "https://www.cs.umb.edu/~pchen/"
    affiliations:
      name: UMASS Boston

bibliography: hf/hf.bib

---
The work on this project is under review in a journal.
## Objective
<img class="float-right w-25" src="{{ page.img | relative_url }}"/>
Understanding chaotic systems are challenging not only for theoretical research but also for many critical applications. Chaotic behavior is found in many nonlinear dynamical systems, such as climate dynamics, weather prediction, and the space-time dynamics of virus spread.  A reliable solution for these systems must handle their complex space-time dynamics and sensitive dependence on initial conditions.

## Proposed Model
We develop a deep learning framework to push the time horizon at which reliable predictions can be made further into the future by better evaluating the consequences of local errors when modeling nonlinear systems.  Our approach  observes  the  future  trajectories  of  initial  errors  at  a  time  horizon  to  model  the  evolution  of  the  loss to  that  point  with  two  major  components:  
- a recurrent  architecture, Error  Trajectory  Tracing, designed to trace the trajectories of predictive errors through phase space
- a training regime, Horizon Forcing, pushes the model’s focus out to a predetermined time horizon. 
