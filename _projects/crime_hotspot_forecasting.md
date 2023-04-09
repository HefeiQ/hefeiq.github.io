---
layout: distill
title: Crime Hot Spot Forecasting
description: In our work on crime hotspots forecasting, we aimed to improve the effectiveness and efficiency of crime prevention strategies by developing a model that could capture latent spatio-temporal features. To achieve this, we integrated two powerful neural network architectures: transposed convolutions and deep recurrent networks. The transposed convolutions were used to learn the spatial spread of features from the input data, while the recurrent network was used to model the temporal evolution. By combining these two architectures, we were able to capture complex spatio-temporal patterns in crime data and generate accurate forecasts of crime hotspots.
img: /assets/img/crime/crime.jpg
start: 2017
publish: 2017
importance: 2
category: research

authors:
  - name: Yong Zhuang
    url: "https://yong-zhuang.github.io"
    affiliations:
      name: UMASS Boston
  - name: Matthew Almeida
    url: "https://matthewalmeida.github.io/"
    affiliations:
      name: UMASS Boston
  - name: Melissa Morabito  
    url: "https://www.uml.edu/fahss/criminal-justice/faculty/morabito-melissa.aspx"
    affiliations:
      name: UMASS Lowell
  - name: Wei Ding
    url: "https://www.cs.umb.edu/~ding/"
    affiliations:
      name: UMASS Boston

bibliography: hf/hf.bib
---
The work on this project has published in ICBK 2017. Take a look at ["Crime hot spot forecasting: A recurrent model with spatial and temporal information"]({{ 'zhuang2017crime/paper.pdf' | prepend: '/assets/pdf/' | relative_url }}) for more details.
## Objective
In recent years, place-based crime prediction has garnered significant attention from researchers. Numerous studies have been conducted on this topic, and some of them have found that in specific areas, there are stable hot spots and flow hot spots that exist simultaneously. Moreover, the measurement of crime hot spots becomes more dynamic and unstable as the time and space scales decrease.  Therefore, capturing the temporal evolution of spatial crime patterns has become crucial in developing effective and efficient crime prevention strategies.

## Proposed Model
<img class="float-left w-50" src="{{ page.img | relative_url }}"/>
Deep recurrent neural networks (RNN) have shown remarkable performance in numerous sequence prediction problems, such as machine translation, contextual parsing, image captioning, and video description. These networks are specially designed to process sequences and capture the temporal evolution of the objects within them. Additionally, some variants like the Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU) have demonstrated an ability to handle long-term dependencies particularly well. Motivated by this, we built [a deep network to forecast crime hot spots by simulating spatial patterns' temporal evolution via embedding spatial information into recurrent architecture]({{ 'zhuang2017crime/paper.pdf' | prepend: '/assets/pdf/' | relative_url }}). We believe that capturing these spatial patterns' temporal evolution can enhance the effectiveness and efficiency of crime prevention strategies. To evaluate the effectiveness of our model, we used call-for-service data provided by the Portland, Oregon Police Bureau (PPB) over a five-year period from March 2012 through December 2016. Our experiment results indicate that our proposed model outperforms several classical machine learning approaches and alternative neural network architectures in forecasting crime hot spots.