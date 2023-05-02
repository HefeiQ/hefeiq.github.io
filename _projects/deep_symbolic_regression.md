---
layout: distill
title: Deep symbolic regression
description: Using a suitable reward mechanism with the reinforcement learning to identify the correct mathematical expression from an exponentially growing space of expressions that may describe a given dataset.
# Reinforcement learning can be leveraged to address the challenge of identifying the correct mathematical expression from an exponentially growing space of expressions that may describe a given dataset. By using a suitable reward mechanism, the reinforcement learning approach encourages the model to explore and find the optimal solution in this vast space of potential mathematical expressions.
img: /assets/img/symbolic_regression/deep_symbolic_regression.jpg
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
### Objective
<img class="float-left w-50" src="{{ 'symbolic_regression/deep_symbolic_regression.jpg' | prepend: '/assets/img/' | relative_url }}"/>
Symbolic regression is a challenging task in both physics and artificial intelligence, requiring the identification of a symbolic expression that accurately fits unknown function data. Although deep neural networks have shown remarkable performance in solving complex tasks, developing deep learning methods for symbolic regression remains an open issue. The key challenge in symbolic regression is the exponential growth of the space of mathematical expressions, which is both discrete (in model structure) and continuous (in model parameters). To find the optimal solution within this space, an appropriate reward mechanism is needed to guide the model in identifying the correct mathematical expression.  It means reinforcement learning is a potential solution for this problem.

