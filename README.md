# NLTk
Apply NLTK to mining and analyse text by using steaming, tokenization
## Introduction

This file discusses the use of the NLTK (Natural Language Toolkit) library in Python for applying text mining and analysis techniques. It explains the concept of NLTK and its importance in natural language processing, as well as some basic methods for preparing text for analysis, such as tokenization, stemming, and lemmatization.

## NLTK Overview

- NLTK is an open-source software library designed to facilitate the development of natural language processing applications in Python.
- NLTK offers powerful capabilities in various areas such as text analysis, classification, named entity recognition, sentiment analysis, and natural language generation.

## Preprocessing Techniques

### Tokenization
The process of breaking down a text into smaller units such as words, symbols, and phrases.

### Stemming
The process of reducing words to their base or root form by removing prefixes and suffixes.

### Lemmatization
The process of determining the base or dictionary form of a word (lemma) using vocabulary and morphological analysis.

## Benefits of Using NLTK
1. Powerful text processing capabilities.
2. Providing a wide range of useful linguistic resources.
##code
import nltk
from nltk.tokenize import word_tokenize
from nltk.stem import PorterStemmer
from nltk.corpus import stopwords

nltk.download('stopwords')
nltk.download('punkt')

stop_words = set(stopwords.words('english'))

text = "Data science is an interdisciplinary field that uses scientific methods, processes, algorithms, and systems to extract knowledge and insights from data."

tokens = word_tokenize(text)
stemmer = PorterStemmer()
stemmed_tokens = [stemmer.stem(token) for token in tokens]
filtered_tokens = [token for token in stemmed_tokens if token.lower() not in stop_words]

print("Original Text: ", text)
print("Stemmed Tokens: ", stemmed_tokens)
print("Filtered Tokens: ", filtered_tokens)
