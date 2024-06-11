---
layout: page
title: Tool to Analyse Public’s Political Opinion
description: Sentimental analysis tool based on BERT, for comparing and getting insights on the french presidential election candidates.
img: 
importance: 1
---

Abstract: Lead a team of 3 in creating a tool that uses sentimental analysis on filtered french tweets to analyze the public's political opinion, comparing candidates, and offering different insights for the presidential elections in France. Trained on data from before the 2017 elections and evaluated on data from before the 2022 elections. Compared 3 different approaches: Logistic Regression (LR), Convolutional-Neural-Network (CNN), Bidirectional Encoder Representations from Transformers (BERT).
Time: 3 months (2021)
Technologies: Python, Jupyter Notebooks, BERT, Octoparse
Contributions:
<ul>
  <li>Data extraction: choosing appropriate tweet filters and using octoparse to scrape results and create datasets.</li>
  <li>Labelling: each tweet needed to be clasified according to its positive/neutral/negative segment towards a candidate.</li>
  <li>Pre-processing: cleaning, tokenization, removing names and direct references, french lemmatization with SpaCy, word embeddings.</li>
  <li>Implementation of the french BERT model for a 86.3% accuracy.</li>
  <li>Graphic representation of results, anomaly detection, and correlation with campaign events.</li>
</ul>
