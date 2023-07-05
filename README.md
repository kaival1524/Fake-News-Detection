# Fake-News-Detection

## Overview of the Problem
The problem of unreliable news being spread rapidly digitally with next to no fact-checking is a immense problem and results in the rampant spread of misinformation. The negative effects of fake news range from uncertainty in the fairness of elections, to damage to the reputation and profitability of individuals and corporations. Market research indicates that as much as \$39 billion is lost annually as a result of uncontrolled fake news\cite{cost}. This large issues establishes a large monetary and societal motivation for the development of effective techniques to detect this issue.

Natural Language Processing techniques have been of great interest to mitigating the effects of fake-news \cite{KHAN2021100032}. The development of such solutions, provide at times super-human levels of fake-news detection with the scalability to scan large portions of the internet. In this paper, we will introduce a novel technique to detect fake news built upon existing work in NLP.

## Overview of Data and Pre-processing
In our pursuit of developing a machine learning model to detect fake-news, we've identified a dataset\cite{Bisaillon_2020a} found on the online Data Science site Kaggle, which provides an aggregated and labeled collections of articles scraped from fake and reputable news sources. This dataset contains data from around 45,000 articles which will allow us to spare a large number of samples for validation as well as counteract the effects of sampling bias from limited sources.

## Data format and cleaning
The data is originally presented in the form of two comma separated tables of real and fake articles. We will combine these two tables into one by adding a (\textit{is\_fake}) column to the table. Each row in the table represents and article, with the columns describing the article being: article title (\textit{title}), article text (\textit{text}), subject, date, and the newly introduced \textit{is\_fake}. Some samples are shown in the below figure.

After inspecting the dataset, a few key issues are aparent. Namely: there are discrepancies between the subject classes in the true and false news sources. Some date fields are malformed, with completely incorrect and unparsable data.


## Feature Selection
While preparing our dataset for the ultimate goal of developing a machine learning classifier, we will need to ensure our data is both correctly formatted and appropriate for the model.
