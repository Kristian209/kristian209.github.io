---
layout: post
title:  "Data-lit: Collections(1.3) Cleansing Data"
date:   2019-02-13 12:49:44 -0800
categories: data lit
---
Today I learned how to clean and prepare text data.

**Cleaning text-data**: A typical pre-processing task for data science and machine learning.
- It consists of getting rid of the less useful  parts of text through stopword
removal, dealing with capitalization, special characters and anything else that
may be useless.

There is a wide-range of text preparation methods that you may need to use.
- The choice of methods depends on your natural language processing task.

In this exercise we used the book "Metamorphosis" by Franz Kafka as our dataset.
(We removed footer & header)

**Step 1**: Sneak a peek at the data
- There were no obvious typos or spelling errors
- There's punctuation
- It's very simple

**Step 2: Whitespace/ Punctuation/ Normalize case**
There are 2 ways to go about this step:
- Manually
- Using a NLTK library

**<Manually>**
1.Load data
2.Tokenization  
- Tokenization describes splitting paragraphs into sentences, or sentences into
   individual words.  
- We split by Whitespace and removed punctuation.  
- If we were to split by words we would get "wasn" and "t" from "wasn't"  
- We used Python 3 string funciton  
- maketrans() - this static method returns a translation table usable for str.translate()  
- translate() - Return a copy of a string in which each character has been mapped  
   through the given translation table
3.Capitalization  
- .lower()  

**<NLTK>**
Natural Language Toolkit
- It provides a high-level API to flexibly implement a variety of cleaning methods

1.Install NLTK
2.Tokenization
3.Filter out punctuation

**Step 3: Stopwords/ Stemming**
1.Filter out Stopwords and pipelines
2.Stemming
 - Stemming is a proccess where words are reduced to a root by removing inflection
   through dropping unnecessary characters, usually a suffix.
 - There is a danger of "over-stemming" where words like "universe" and "university"
   are reduced to the same root of "univers"

**Step 4: Other Tools**
1.Lemmatization
 - Lemmatization is an alternative to removing inflection
 - It is more accurate but slower
 - Stemming may be more useful in queries for databases whereas Lemmatization may
   work much better when determining text sentiment.
2.Word Embedding/ Text Vectors
 - Word Embedding is the modern way of representing words as vectors.
 - The aim of word embedding is to find a series of high dimensionality vectors(one
   for each word) that represents the relation of words so that semantically related
   words are closer together in that high dimensional space.
