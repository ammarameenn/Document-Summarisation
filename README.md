# Document-Summarisation
Text generation, which could be used, for instance, in text summarization, is one of the difficulties in natural language processing and comprehension. Actually, it entails comprehending the information a text conveys and condensing it into a brief summary that incorporates the essential, pertinent information. It is obvious that a model works effectively on a text that is condensed and has just clear information and little noise. In this situation, we can use some extractive summarizers as the input of the summarization model to extract significant portions from a given text. I decided to use TFIDF vectoriser to condense the text and extract the most crucial sentences.
This repository will walk you through two different approaches for summarizing text named abstractive and extractive summarisation using very famous techniques TF-IDF and transfer learning.
## Notebook Content

* Loading Dataset
* Preprocessing Datatset
* Extractive Summarization Approach
  * TF-IDF summarizer
* Abstractive summarization Approach
  * t5-base Transformer
### Loading Dataset
The NLTK corpus is a massive dump of all kinds of natural language data sets. Here I am loading Inaugral Dataset which includes Welcome speech of American presidents from 1789 to 2021.

I am in this notebook summarizing Joe Biden's Speech given by him.
### Text PreProcessing 
From tokenisation on sentence and word level to removing any HTML tags and all the basic preprocessing starts from here. All the contractions used in general english are also taken care of in this part.
### Extractive Summarisation Approach

* This method does not create new words or phrases, it just takes the already existing words and phrases and presents only that. You can imagine this as taking a page of text and marking the most important sentences using a highlighter.

* Extractive summarization methods work just like that. It takes the text, ranks all the sentences according to the understanding and relevance of the text, and presents you with the most important sentences. 

* There are many techniques to score sentences. Here I am using TF-IDF short for term frequency–inverse document frequency, is a numerical statistic that is intended to reflect how important a word is to a document in a collection or corpus.
After getting Sentence Scores, I average the score of all the sentences and took into account only 50 most important sentences from Joe Biden's speech.
### Abstractive summarization
* Up untill nnow we have extractive summary.
* Now I am using already pre trained model based on transformers called t5-base to train another model to create a short abstract of extractive summary.
