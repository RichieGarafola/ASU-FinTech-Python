# Unit 12—Tales from the Crypto

![Stock Sentiment](Images/sentimental.jpeg)

## Background

There's been a lot of hype in the news lately about cryptocurrency, so you want to take stock, so to speak, of the latest news headlines regarding Bitcoin and Ethereum to get a better feel for the current public sentiment around each coin.

In this assignment, you will apply natural language processing to understand the sentiment in the latest news articles featuring Bitcoin and Ethereum. You will also apply fundamental NLP techniques to better understand the other factors involved with the coin prices such as common words and phrases and organizations and entities mentioned in the articles.

Complete the following tasks:

1. [Sentiment Analysis](#1---Sentiment-Analysis)
2. [Natural Language Processing](#2---Natural-Language-Processing)
3. [Named Entity Recognition](#3---Named-Entity-Recognition)

---

## Files

[Starter Notebook](Starter_Code/crypto_sentiment.ipynb)

---

## Instructions

### 1 - Sentiment Analysis

Use the [newsapi](https://newsapi.org/) to pull the latest news articles for Bitcoin and Ethereum and create a DataFrame of sentiment scores for each coin.

Use descriptive statistics to answer the following questions:

> Which coin had the highest mean positive score?
>
> Which coin had the highest negative score?
>
> Which coin had the highest positive score?



### 2 - Natural Language Processing

In this section, you will use NLTK and Python to tokenize text, find n-gram counts, and create word clouds for both coins. 

#### Tokenize

Be sure to:

1. Lowercase each word.
2. Remove punctuation.
3. Remove stop words.

#### N-grams

Next, look at the ngrams and word frequency for each coin.

1. Use NLTK to produce the ngrams for N = 2.
2. List the top 10 words for each coin.

#### Word Clouds

Finally, generate word clouds for each coin to summarize the news for each coin.

![btc-word-cloud.png](Images/btc-word-cloud.png)

![eth-word-cloud.png](Images/eth-word-cloud.png)


### 3 - Named Entity Recognition

In this section, you will build a named entity recognition model for both coins and visualize the tags using SpaCy.

![btc-ner.png](Images/btc-ner.png)

![eth-ner.png](Images/eth-ner.png)



### Resources

[Vader Sentiment Analysis](http://www.nltk.org/howto/sentiment.html)


### Hints and Considerations

The free developer version of the News API limits the total daily requests, so be careful not to exceed the free limits.

### Submission

* Use the starter Jupyter Notebook provided to conduct the NLP analysis and host the notebook in a GitHub repository.

* In your GitHub repository, include a ReadMe file that uses Markdown to summarize your homework.

* Submit the link to your GitHub project to Bootcamp Spot.

---
### Requirements

#### Sentiment Analysis  (30 points)

##### To receive all points, your code must:

* Determine the coin with Highest Mean Positive Score. (10 points)
* Determine the coin with Highest Negative Score. (10 points)
* Determine the coin with Highest Positive Score. (10 points)

#### Natural Language Processing  (30 points)

##### To receive all points, your code must:

* Use NLTK to lower case words, remove punctuation and remove stopwords. (8 points)
* Use NLTK to produce n-grams. (8 points)
* List the top 10 words for each Coin. (7 points)
* Generate a Word Cloud for each Coin summarizing the news for each Coin. (7 points)

#### Named Entity Recognition  (10 points)

##### To receive all points, your code must:

* Build a Named Entity Recognition model for both coins - Bitcoin and Ethereum - and visualized the tags for each coin using SpaCy. (10 points)

#### Coding Conventions and Formatting (10 points)

##### To receive all points, your code must:

* Place imports at the beginning of the file, just after any module comments and docstrings and before module globals and constants. (3 points)
* Name functions and variables with lowercase characters and with words separated by underscores. (2 points)
* Follow Don't Repeat Yourself (DRY) principles by creating maintainable and reusable code. (3 points)
* Use concise logic and creative engineering where possible. (2 points)

#### Deployment and Submission (10 points)

##### To receive all points, you must:

* Submit a link to a GitHub repository that’s cloned to your local machine and contains your files. (5 points)
* Include appropriate commit messages in your files. (5 points)

#### Code Comments (10 points)

##### To receive all points, your code must:

* Be well commented with concise, relevant notes that other developers can understand. (10 points)

---

© 2021 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
