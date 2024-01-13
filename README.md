## Natural Language Processing (NLP)

Follow the chart given below : 

<img width="700" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/8527bde4-2af1-4f4a-9601-2c9f11f8b403">

### Text Preprocessing - 1 : Tokenization, Lemmatization, Stop Words & POS 

#### Stemming and Lemmatization

**Stemming** - Process of reducing infected words to their word stem. \
	- Without meaning \
	- Lesser time to get to root word. \
	- Sentiment classifier, positive negative analysis, gmail spam classifier \
**Problem :** Produced intermediate representation of the word may not have any meaning.\
**Eg.:** intelligent -> intelligen, final -> fina etc\
<img width="250" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/471e5871-01d8-409c-a5b1-19e5043d8d23">
<img width="275" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/e6f4abf4-c960-45ab-97dc-cb7e75ba35c0">
<img width="215" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/d63b41fe-38dd-409e-b3a4-b93a68bee95a">
\
\
**Lemmatization** - is the process of grouping together different inflected form of same words.\
	- with meaning\
	- More time to get the root word.\
	- Chat bots, QnA application.\
**Eg.:**\
<img width="275" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/aef4b38f-8a3e-4400-b928-a83a59c948d5">
<img width="210" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/a6d4ebbf-2431-4288-8ff8-03693daec3ea">
\
\
**Stopwords** - A set of commonly used words in a language.\
**Eg.:** "a", "is", "the", "are", "them"


### Text Preprocessing - 2 : Bag of Words, TF-IDF, Unigrams, Bigrams, n-grams

#### Bag of Words

It’s a model used to preprocess the text by converting it to bag of words, which keeps a count of the total occurrences of most frequently used words.

<img width="700" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/84517f96-0be0-45c1-9df2-453203109acf">
<img width="710" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/fc15c35a-d8be-414c-a771-8e368b3d216c">

 We convert the frequency representation into vectors using Bag of Words. The Binary Bag of Words is representing the word with 0 or 1. In the Normal Bag of Words if a word count is more than one then that specific number is used to represent the count.

**Disadvantage :** \
Every word in a sentence is given equal importance.

#### TF - IDF ( Term Frequency - Inverse Document Frequency )

 After doing stemming and lemmatization, consider three sentences\
 \
<img width="350" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/14c3900a-65c0-4ceb-96bc-556ba4271e0c">\
 \
 Frequency representation of words:\
 \
<img width="350" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/58091857-2d11-4640-aaa3-8e56320fa3e9">\
 \
 Applying TF-IDF to this, the formula's used is,\
 \
 <img width="420" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/b30b12bf-3541-4cfb-a240-426690e66c17">
 <img width="290" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/f4358b9c-d68a-412b-a98a-4440c3c63d87">
 \
 \
 Finally,\
 \
 <img width="80" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/f6e38417-2837-44f2-9b39-5647e2ead4ed">

 We apply these formula into above sentences,\
\
 <img width="350" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/ef3a341b-30dd-44ae-88fe-e3ab52762a32">
 <img width="150" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/a9af2fed-69a5-4389-82e0-f4a6759f9a7d">
 <img width="370" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/e966d095-e309-4ae6-ad6e-3521f23eb740">

 ### Text Preprocessing - 3 : Gensim, Word2Vec, AvgWord2Vec

 #### Word2Vec
 **Problems with BOW and TF-IDF**
- Both BOW and TF-IDF approach semantic information is not stored. TF-IDF gives importance to uncommon words.\
	**Eg. :** Consider the 3-4 sentences, the number of times each word get repeated is not given that much importance.
- There is definitely chance of over fitting.

  **Solution - Word2Vec**
- In this specific model, each word is basically represented as a vector of 32 or more dimension instead of a single number.
- Here the semantic information and relation between different words is also preserved.

  **Visual Representation**\
  \
Consider a two-dimensional graph, where each word can be plotted. Those word which are related will have smaller distance in the space
( Eg. : Man and Woman), and those with larger distance in the space are not that much related.

<img width="340" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/07237f75-ac87-4f85-9410-07aa2db9e907">
<img width="436" alt="image" src="https://github.com/Thejas-294/NLP/assets/79050445/2af1b086-8b94-4b1e-87f2-45bfc35832bd">

**Steps to Create Word2Vec**
- Tokenization of the sentences
- Create Histograms
- Take most frequent words
- Create a matrix with all the unique words. It also represent the occurrence relation between the words.






 


 





















