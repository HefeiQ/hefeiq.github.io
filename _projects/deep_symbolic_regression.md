---
layout: distill
title: Deep symbolic regression
description: using deep neural networks to estimate the underlying mathematical expressions describing a given dataset.
img: /assets/img/symbolic_regression/dsr.jpg
start: 2021
publish: 

importance: 3
category: research

authors:
  - name: Yong Zhuang
    url: "https://yong-zhuang.github.io"
    affiliations:
      name: UMASS Boston
  - name: Zihan Li
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
<img class="float-left w-25" src="{{ 'symbolic_regression/dsr.jpg' | prepend: '/assets/img/' | relative_url }}"/>
One of the core challenges of physics and artificial intelligence is to find a symbolic expression that matches the data of an unknown function, called symbolic regression. Although deep neural networks have shown impressive performance in solving complex tasks, deep learning methods for symbolic regression are still open. The major challenge of symbolic regression is that the space of mathematical expressions is discrete (in model structure) and continuous (in model parameters) and growing exponentially with the length of the expression. A suitable reward mechanism could inspire the model to identify the correct mathematical expression from the expression space. It means reinforcement learning is a potential solution for this problem.

