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
1.) creating text corpus tm::Vcorpus
2.) cleaning text tm::tm_map
  * lower letters
  * remove: numbers, stopwords, punctuation, remove white space
  * steming words
3.) creating sparse matrix tm::TermDocumentMatrix (DTMs)
4.) creating test(75%) and train(25%) datasets
5.) world clouds (reliable, fake)
6.) filtereing DTMs for only frquent words
7.) applying the algorithm on test and train datasets

## Results
             | actual 
   predicted | notreliable |    reliable |   Row Total | 
-------------|-------------|-------------|-------------|
 notreliable |        2100 |         940 |        3040 | 
             |       0.801 |       0.365 |             | 
-------------|-------------|-------------|-------------|
    reliable |         522 |        1638 |        2160 | 
             |       0.199 |       0.635 |             | 
-------------|-------------|-------------|-------------|
Column Total |        2622 |        2578 |        5200 | 
             |       0.504 |       0.496 |             | 
-------------|-------------|-------------|-------------|

i.e. accuracy only 71%


