---
layout: page
title: Crime Hot Spot Forecasting
description: A recurrent neural network to forecast crime hot spots.
img: /assets/img/crime/crime.jpg
importance: 2
category: research
---
<div class="post">
    <div class="profile float-left w-50">
        <img class="img-fluid" src="{{ page.img}}"/>
    </div>
</div>
Place-based Crime prediction has become an area of significant research interest in recent years. Some studies have found that stable hot spots and flow hot spots always exist simultaneously in a specific area, and crime hot spots become more dynamic and unstable as the measurement time and space scale decrease. Therefore, to make specific crime prevention strategies effective and efficient, capturing the temporal evolution of spatial crime patterns has become a great demand.

Deep recurrent neural networks (RNN), which have shown impressive performance in several sequence prediction problems, including machine translation, contextual parsing, image captioning, and even video description, are designed to process sequences and capture the temporal evolution of the objects. In addition, some variants like the Long Short-Term Memory (LSTM) and Gated Recurrent Unit(GRU) can deal with long-term dependencies well. We propose [a recurrent neural network to forecast crime hot spots by simulating spatial patterns' temporal evolution with spatial information embedding]({{ 'zhuang2017crime/paper.pdf' | prepend: '/assets/pdf/' | relative_url }}). We evaluate the model using call-for-service data provided by the Portland, Oregon Police Bureau (PPB) for five years, from March 2012 through December 2016. The experiment results show that our model outperforms several classical machine learning approaches and alternative neural network architectures.
