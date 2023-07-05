# Fake News Detection

## Overview of the Problem
The problem of unreliable news being spread rapidly digitally with next to no fact-checking is a immense problem and results in the rampant spread of misinformation. The negative effects of fake news range from uncertainty in the fairness of elections, to damage to the reputation and profitability of individuals and corporations. Market research indicates that as much as $39 billion is lost annually as a result of uncontrolled fake news. This large issues establishes a large monetary and societal motivation for the development of effective techniques to detect this issue.

Natural Language Processing techniques have been of great interest to mitigating the effects of fake-news \cite{KHAN2021100032}. The development of such solutions, provide at times super-human levels of fake-news detection with the scalability to scan large portions of the internet. In this project, we will introduce a novel technique to detect fake news built upon existing work in NLP.

## Model Design
With a solid foundation of clean and relevant predicting features, the next decision is designing an appropriate model architecture and hyperparamaters. Due to the sequentual and inter-related nature of textual data, a Recurrent Neural Network with Long Short Term Memory (LSTM) has been shown to perform very well for article text Sherstinsky2018-vb. Prior to training we tokenize the text, by converting words into numbers based on frequency and pad the sequences to provide uniform lengths to the model.Additionally, the model needs to accept numeric inputs for the sentiment analysis results and subject results. This was achieved by added a separate input layer and using a Tensorflow merge layer to concatenate the output of the LSTM layers to the inputs in a way where the gradients can still be computed.

## Evaluation and Summary
In evaluating our model, we primarily used a Confusion matrix on the validation set. From the Confusion Matrix, we see that we had 4243 True Negatives, 4 False Positives, 2 False Negatives, 4731 True Positives. From this, we found that our model had a precision of 99.92 percent, a recall of 99.96 percent, and an accuracy of 99.93 percent. However, there may have been data leakage in our model from direct unintended markers in the text identifying the news source rather than the actual content. Which may inflate the accuracy on the validation set. 

![confusion_matrix](https://github.com/kaival1524/fake-news-detection/assets/69801409/6945dceb-60c3-4cc4-86bb-178c541334bf)
