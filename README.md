# Exploratory Topic Modelling Using Python
##### by Mike Bryant and Maria Dermentzi 

This notebook aims to walk readers through the process of topic modelling in Python and accompanies the article (to be) published in the European Holocaust Research Infrastructure (EHRI) Document Blog entitled "Exploratory Topic Modelling Using Python".

#### Credits:
The transcripts that form the corpus in this tutorial were obtained through the [United States Holocaust Memorial Museum](https://www.ushmm.org/) (USHMM).

## What is Topic Modelling?
Topic modelling is a technique by which documents within a corpus are clustered based on the manner in which certain groups of terms are used together within the text. The commonalities between such term groupings tend to form what we would normally call “topics”, providing a way to automatically categorise documents by their structural content, rather than any a priori knowledge system. Topic modelling is generally most effective when a corpus is large and diverse, so the individual documents within in are not too similar in composition. In EHRI, of course, we focus on the Holocaust, so documents available to us are naturally restricted in scope. It was an interesting experiment, however, to test to what extent a corpus of Holocaust-related documents was able to be topic modelled, and what “topics” emerged within them.

The specific type of topic modelling we’re looking at is called latent Dirichlet allocation (LDA), subject of an influential paper by David Blei et al (2003).  

## The Dataset/Putting Together the Corpus
We were on the lookout for datasets that would be easily accessible and, for convenience, predominantly in English. One such dataset was the USHMM extensive collection of [oral history testimonies](https://www.ushmm.org/online/oral-history/detail.php?SurveyId=226&letter=U&ord=127), for which there are a considerable number of textual transcripts. The museum’s total collection consists of over 80,703 testimonies, 41,695 of which are available in English, with 2,894 of them listing a transcript.  

Since there is not yet a ready-to-download dataset that includes these transcripts, we had to construct our own. Using a web scraping tool, we managed to create a list of the links pointing to the metadata (including transcripts) of the testimonies that were of interest to us. After obtaining the transcript and other metadata of each of these testimonies, we were able to create our dataset and curate it to remove any unwanted entries. For example, we made sure to remove entries with restrictions on access or use. We also removed entries with transcripts that consisted only of some automatically generated headers and entries which turned out to be in languages other than English. The remaining 1,873 transcripts form the corpus of this tutorial — a small, but still decently sized dataset.

## How to use
You can either dowload the repository and run the Jupyter notebook on your local device (you might need to install any libraries that are not already installed in your device) or read the contents of the [notebook](https://github.com/mdermentzi/ehri-topic-modelling-guide/blob/main/USHMM_Oral_Testimonies_Topic_Modelling.ipynb) without running it.  

You can also view the notebook in [Google Colab](https://colab.research.google.com/drive/1XgcO9cHaBrMwfO1bjmkd0tFuw0ExHXdc?usp=sharing) but it will not be possible to import the provided datasets.

## Visualisations
[Link to the LDAvis for the three-topic model](/model_3_topics.html)  
[Link to the LDAvis for the six-topic model](/model_6_topics.html)

## References:
Blei, D. M. et al. (2003) Latent dirichlet allocation. Journal of machine Learning research. 3 (Jan), 993–1022.