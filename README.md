NLP Techniques on Text Data in Python
Indraniel Wandkar
PRN: - 25070123156

#1. Tokenization

import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('punkt_tab')


     
[nltk_data] Downloading package punkt to /root/nltk_data...
[nltk_data]   Unzipping tokenizers/punkt.zip.
[nltk_data] Downloading package stopwords to /root/nltk_data...
[nltk_data]   Unzipping corpora/stopwords.zip.
[nltk_data] Downloading package wordnet to /root/nltk_data...
[nltk_data] Downloading package punkt_tab to /root/nltk_data...
[nltk_data]   Unzipping tokenizers/punkt_tab.zip.
True

# Word Tokenization

from nltk.tokenize import word_tokenize

text = "Natural Language processing is interesting"

tokens = word_tokenize(text)

print(tokens)
     
['Natural', 'Language', 'processing', 'is', 'interesting']

# Sentence Tokenization

from nltk.tokenize import sent_tokenize

text = "Python is easy. It is widely used in data science."

sentences = sent_tokenize(text)

print(sentences)
     
['Python is easy.', 'It is widely used in data science.']

from nltk.draw.util import Text
#Stop Word Removal
# Stop word such as is, the ,and, in are removed

from nltk.corpus import stopwords
stop_words = set(stopwords.words('english'))

words = word_tokenize (text)

filtered_words = [w for w in words if w.lower() not in stop_words]


print(filtered_words)
     
['Python', 'easy', '.', 'widely', 'used', 'data', 'science', '.']

# stemming
# Stemming reduces words to their root fro,

from nltk.stem import PorterStemmer

stemmer = PorterStemmer()

words = ["Playing", "Studies", "running", "gone","watched", "coding"]

for w in words:
  print(stemmer.stem(w))
     
play
studi
run
gone
watch
code

#Lemmatization
#Lemmatization convert words to their dictionary form.
from nltk.stem import WordNetLemmatizer
Lemmatizer = WordNetLemmatizer()
print(Lemmatizer.lemmatize("writing"))
print(Lemmatizer.lemmatize("studies"))
print(Lemmatizer.lemmatize("best"))
print(Lemmatizer.lemmatize("running"))
print(Lemmatizer.lemmatize("coding"))


     
writing
study
best
running
coding

#Part-of-speech (POS) Tagging
# POS tagging identifies grammatical roles of words
import nltk
nltk.download('averaged_perceptron_tagger')
nltk.download('averaged_perceptron_tagger_eng')
     
[nltk_data] Downloading package averaged_perceptron_tagger to
[nltk_data]     /root/nltk_data...
[nltk_data]   Unzipping taggers/averaged_perceptron_tagger.zip.
[nltk_data] Downloading package averaged_perceptron_tagger_eng to
[nltk_data]     /root/nltk_data...
[nltk_data]   Unzipping taggers/averaged_perceptron_tagger_eng.zip.
True

from nltk import pos_tag

words = word_tokenize("Python is a powerful programming language")
pos_tag1 = pos_tag(words)
print(pos_tag1)
     
[('Python', 'NNP'), ('is', 'VBZ'), ('a', 'DT'), ('powerful', 'JJ'), ('programming', 'NN'), ('language', 'NN')]


#Word Frequency count
from nltk.probability import FreqDist

words = word_tokenize(text)
fd = FreqDist(words)
print(fd.most_common())
     
[('is', 2), ('.', 2), ('Python', 1), ('easy', 1), ('It', 1), ('widely', 1), ('used', 1), ('in', 1), ('data', 1), ('science', 1)]
