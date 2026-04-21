# Experiment 16– NLP Techniques on Text Data in Python

*Indraniel Wandkar*
*PRN:* 25070123156

---

## Aim

To study and implement various Natural Language Processing (NLP) techniques in Python using the NLTK library, including tokenization, stop word removal, stemming, lemmatization, part-of-speech tagging, and word frequency analysis.

---

## Theory

Natural Language Processing (NLP) is a field of artificial intelligence that focuses on enabling computers to understand, interpret, and process human language. It plays a crucial role in applications such as text analysis, chatbots, sentiment analysis, and machine translation.

The NLTK (Natural Language Toolkit) is a popular Python library used for working with human language data. It provides easy-to-use interfaces for various NLP tasks.

The following techniques were implemented in this experiment:

### 1. Tokenization

Tokenization is the process of breaking text into smaller units such as words or sentences.

* *Word Tokenization* splits text into individual words.
* *Sentence Tokenization* splits text into sentences.

### 2. Stop Word Removal

Stop words are commonly used words such as is, the, and, in, which do not carry significant meaning. Removing them helps in focusing on important words.

### 3. Stemming

Stemming reduces words to their root or base form by removing suffixes.
Example:

* playing → play
* studies → studi

### 4. Lemmatization

Lemmatization converts words to their meaningful base (dictionary) form. It considers the context and produces valid words.
Example:

* studies → study
* running → running

### 5. Part-of-Speech (POS) Tagging

POS tagging assigns grammatical labels to words such as noun, verb, adjective, etc.
Example:

* Python → Proper Noun (NNP)
* is → Verb (VBZ)

### 6. Word Frequency Count

This technique counts how often each word appears in a text. It helps identify the most common words and patterns in the data.

---

## Conclusion

Thus, the implementation of various NLP techniques using Python and the NLTK library was successfully performed. The experiment demonstrated how to preprocess text data through tokenization, remove unnecessary words, reduce words to their base forms using stemming and lemmatization, identify grammatical roles using POS tagging, and analyze word frequency. These techniques are fundamental in building efficient NLP and text analysis applications.
