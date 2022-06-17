# Exploratory Topic Modelling Using Python
##### by Mike Bryant and Maria Dermentzi 

This notebook aims to walk readers through the process of topic modelling in Python and accompanies the article (to be) published in the European Holocaust Research Infrastructure (EHRI) Document Blog entitled "Exploratory Topic Modelling Using Python".

#### Credits:
The transcripts that form the corpus in this tutorial were obtained through the [United States Holocaust Memorial Museum](https://www.ushmm.org/) (USHMM).

## What is Topic Modelling?
Topic modelling is a technique by which documents within a corpus are clustered based on the manner in which certain groups of terms are used together within the text. The commonalities between such term groupings tend to form what we would normally call “topics”, providing a way to automatically categorise documents by their structural content, rather than any a priori knowledge system. Topic modelling is generally most effective when a corpus is large and diverse, so the individual documents within in are not too similar in composition. In EHRI, of course, we focus on the Holocaust, so documents available to us are naturally restricted in scope. It was an interesting experiment, however, to test to what extent a corpus of Holocaust-related documents was able to be topic modelled, and what “topics” emerged within them.

The specific type of topic modelling we’re looking at is called latent Dirichlet allocation (LDA), subject of an influential paper by David Blei et al (2003).

## The Dataset/Putting Together the Corpus
The dataset used in this tutorial comprises transcripts of testimonies found in the oral history collections of the USHMM. Specifically, we were interested in testimonies the transcripts of which were in English. Since there is not a ready-to-download dataset that includes these transcripts, we had to use a web scraping tool to put together a list of the links to the metadata of the testimonies that were of interest to us, including their associated transcripts. After obtaining the transcript and other metadata of each testimony, we had to filter out the dataset to remove the records that had restrictions on their access or use. We also removed any records with empty transcripts or with transcripts that consisted only of some automatically generated headers. Finally, through trial and error, it came to our attention that one of the resulting topics included words in German or Dutch, such as the word "nicht". By searching for the word "nicht" within the transcripts, we were able to locate at least three transcripts in languages other than English that infiltrated our dataset, which was supposed to comprise transcripts only in English. These entries were also removed. The resulting collection of transcripts forms the corpus that this tutorial is based on.

## How to use
You can either dowload the repository and run the Jupyter notebook on your local device (you might need to install any libraries that are not already installed in your device) or read the contents of the [notebook](https://github.com/mdermentzi/ehri-topic-modelling-guide/blob/main/USHMM_Oral_Testimonies_Topic_Modelling.ipynb) without running it.  

You can also view the notebook in [Google Colab](https://colab.research.google.com/drive/1XgcO9cHaBrMwfO1bjmkd0tFuw0ExHXdc?usp=sharing) but it will not be possible to import the provide datasets.