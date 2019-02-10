---
layout: post
title:  "Data-lit: Collections(1.1) Sentiment Analysis"
date:   2019-02-09 20:47:44 -0800
categories: data lit
---
In 1.1 we were walked through how to analyze sentiment through text gathered from
tweets about a certain product. In the video the product chosen was an Apple Watch.
I decided to go with Air Pods to replicate the process with a different product.

Sentiment Analysis is a technique that involves building systems that can identify
and extract opinions from text. It can be rule-based, matching words with sentiment
scores from a lexicon or Automatic, where a trained pattern matching algorithm will
predict a word's sentiment.

Automatic approach
- Pros: Scalable, more accurate
- Cons: Requires training Data

Rule-Based approach
- Pros: No training data required, easy to debug
- Cons: Not as accurate

We built a sentiment analyzer in a few lines of Python using the Twitter API and
the Vader Python Framework.

Project code: https://github.com/Kristian209/Data-lit/blob/master/Sent_Analysis.ipynb
