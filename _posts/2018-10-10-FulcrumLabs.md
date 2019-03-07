---
title: "Fulcrum Labs Internship"
date: 2018-10-10
tags: [Internship]
header:
  #image: images/Experiences/JPL/JPL_front.png
excerpt: "Fulcrum Labs"
mathjax: "true"
---
I am currently a Data Science intern for Fulcrum Labs, a start up developing an adaptive learning platform. During my first quarter at the company I devised a natural language processing (NLP) algorithm that will determine if a student's response to a question is related to a body of text they were to read. Furthermore, I prototyped an algorithm that will assign a performance score to a student given a report from an instructor about a student's behavior in class. This performance score and be augmented by how well they complete courses on the platform.

I am currently working on a prediction model that will, based on how a student chooses to do with their time on the Fulcrum Platform, determine how much time it will take for as student to complete a course. Using *keras*, I implemented a Long Short Term Memory (LSTM) to predict how much time a student will spend on a course. The model I made for this model can be seen below.

```python
multi_model = Sequential()
multi_model.add(LSTM(100, activation = 'relu', input_shape = (train_X.shape[1], train_X.shape[2]), return_sequences = True))
multi_model.add(Dropout(.01))
multi_model.add(LSTM(100, activation = 'relu', input_shape = (train_X.shape[1], train_X.shape[2]), return_sequences = False))
multi_model.add(Dropout(.01))
multi_model.add(Dense(1))
multi_model.compile(loss='mae', optimizer='adam')
```
 So far, I have trained it on the data from one student, and I am working on having it train for multiple students to improve predictions. The prediction I made can be seen in the plot below. My model captured the overall behavior of the data, but it could be improved.

<div style="text-align:center"><img src="{{ site.baseurl }}/images/Experiences/Fulcrum/LSTMPrediction.png"></div>

This internship required a lot of independent research and work. During my research I have played around with various algorithms for gaining insight from data such as Support Vector Machines (SVM) and Google's Page Rank algorithm. Along the way, I learned how to clean up and structure my data in order to implement these algorithms.
