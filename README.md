# naive-bayes
Utilizing the Naive Bayes Algorithm to Predict Reliable vs. Not-realiables news


## About the Project:
* Utilizing e1071::naiveBayes on 20800 news to predict fake vs. reliable news.
* The project serves as my first encounter with the Bayesian Algorithm.
* The algorithm faciliates conditional probability. Specifically, appeareance of specific words in news should be the condition of the probability.
* The code is written in R Markdown. Sources Machine Learning with R; ISBN: 978-1-78439-390-8

## Dataset
* Dataset available at Kaggle: https://www.kaggle.com/c/fake-news/rules
* It contains 20800 news articles of various length.
* Source and method of data collection is unknown

## Methodology
* creating text corpus tm::Vcorpus
* cleaning text tm::tm_map
  * lower letters
  * remove: numbers, stopwords, punctuation, remove white space
  * steming words
* creating sparse matrix tm::TermDocumentMatrix (DTMs)
* creating test(75%) and train(25%) datasets
* world clouds (reliable, fake)
* filtereing DTMs for only frquent words
* applying the algorithm on test and train datasets

## Results
Accuracy only 71%
To improve the model, I plan to fileter fo specific sentiments. 


