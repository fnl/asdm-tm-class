Statistical Text Mining in Python
=================================

This repository contains the PDF slides, Jupyter notebooks, and some software/data for an in-depth course on statistical [Text Mining and NLP](http://fnl.es/an-introduction-to-statistical-text-mining.html) that is part of the [Advanced Statistics and Data Mining Summer School](http://www.dia.fi.upm.es/ASDM) held annually in Madrid, Spain.
The repo provides reference material for most of the common text mining and language processing techniques, taking you from the very basics to the state of the art - or simply should help you decide if this class is "for you."
The two main differences to the actual class are (a) that the animations that are used to explain more complex algorithms/slides (locality sensitive hashing, dependency parsing, etc.) are missing and (b) you obviously don't get my in-depth explanations and discussions of the slides you'd enjoy when visiting the class.

Apart from the full [Jupyter](http://jupyter.org/) stack with Python **3.x**, running the notebooks requires a working installation of several packages described below.
For example, the [Natural Language ToolKit](http://www.nltk.org/), version 3.x (i.e., the latest stable release), which can be installed using `pip install nltk` or via the Continuum Analytics [Anaconda](http://continuum.io/downloads) Python distribution: `conda install nltk` .
In general, the NLTK is a very useful resouce for budding text miners and language processing experts to learn the ropes.
Similary, you should have [`gensim`](http://radimrehurek.com/gensim/index.html) installed, which is probably the most beatuiful "hidden gem" for text mining that you can find in the Python world, among a few other libraries.
As prepartion before coming to the class, installing (recommended: Anaconda) Python and having looked through notebooks 1-3, and possibly 4 and 5, is certainly helpful.

To view the notebooks online, you can access them via the [Jupyter notebook viewer](https://nbviewer.jupyter.org/), by using the Git URLs in this repository, or installing a [browser extension](https://jiffyclub.github.io/open-in-nbviewer/) for Firefox, Chrome, or Safari that opens the GitHub page in the viewer format.

Introduction
------------

There are three introductory notebooks that students are encouraged to study before visiting the class:

1. There is a quick notebook to familiarize yourself with [Jupyter notebooks](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/01_Jupyter.ipynb) in general.
1. Check if your Python skills are in shape: You should understand [most of this](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/02_Python_overview.ipynb), otherwise you might want to first brush up a bit on your Python expertise.
1. Finally, a quick introduction to [the basics of NLTK and NumPy](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/03_NLTK_and_NumPy_overview.ipynb) that is recommended for all but experts familiar with the two libraries.

During this course, we will be using numerous Python modules; The more NLP/text mining-oriented ones are:

* [`nltk`](http://www.nltk.org)
* [`gensim`](http://radimrehurek.com/gensim/index.html)
* [SciKit-Learn](http://scikit-learn.org/) (`sklearn`)
* [`spacy`](https://spacy.io/)
* [`segtok`](https://github.com/fnl/segtok)
* [`pytextrank`](https://github.com/ceteri/pytextrank) - although nowadays I would recommend using [`yake`](https://pypi.org/project/yake/)
* [`keras`](https://keras.io/)

Keras is only used to demonstrate how to plug word embeddings (representation learning) into a deep learning framework ([Keras](https://keras.io/)), and then run a text classification task with a Convolutional Neuronal Network (CNN) model.
(Obviously, those interested in deep learning should have visited the excellent course on neural networks (C05) the week before, as well as probably C01, C04, and C07, and C12, which are all about statistical learning techniques commonly used in text mining and NLP.)
And, the notebooks make a quick glance at some of the [Stanford CoreNLP](https://stanfordnlp.github.io/CoreNLP/) tools, so having Java installed is necessary to run those examples.

Lecture Overview
----------------

The introduction refreshes the basic concepts of machine learning and statistics that matter in the context of this course.
It also introduces all the text mining- and NLP-specific terminology that will be used throughout the course.

The second "chapter" then will cover information retrieval and similarity measures:
The IR part introduces the concept of an inverted index, (count/index-based) word vectors, TF-IDF weighting, and cosine similarity, among other topics.
That is, you will be familiarized with how search engines work, at least from a 10,000 feet birds-eye view.

The following classification section will present all the tools that are needed to categorize text.
We will focus particularly on understanding the concept of maximum entropy (i.e., logistic regression), at it turns out to be a recurrent theme in this domain.
And we will spend some time to familiarize ourselves with the most important element of machine learning: Model evaluation.
In particular, we will look at ways of evaluating the performance of result sets, but also how to compare ranked lists.

As the next leg, we take a look at some unsupervised techniques that are commonly used when working with text.
The tools presented here are particularly useful when you cannot or do not need to generate annotated datasets to train classifiers.
After an overview of algorithmic methods to establish string similarity, we will look at a highly efficient approach to hashing similar texts (Locality Sensitive Hashing, LSH).
This part will also introduce sentence segmentation and collocations, and looks into Latent Semantic Indexing and Latent Dirichlet Allocation for clustering.

The program then dives into possibly the most important concept of modern text mining and natural language understanding: Representation learning.
You will learn what word embeddings are, where they "came from", how the most common (semi-) predictive models work (word2vec, Glove, FastText), and how to extend word embeddings to sentences, paragraphs, and documents.
To put this into context, representation learning is the stepping stone towards deep learning in natural language processing and a simple CNN classifier is used to exemplify this.

That then finally brings us to the first truely natural language processing-focused technique: Language modeling.
We will only give it a brief look, to understand the principles of a Markov model, and introdcue the common approach to measuring language model performance: Perplexity.
This should help particpants understand the difference between a "regular" RNN cell and the concept of Long-Short Term Memory (LSTM) that allow us to integrating over a word's context to generate its embedding.
We will see that by training language models on raw text, a model can "learn" the structure of language on its own, while this knowledge can later be _transferred_ to downstream tasks - a concept that has revolutionized how modern NLP is done. 
Without going into the technical details (out of scope) we will close this topic by discussing how the Transformer architecture with self-attention allows a feed-forward network to have the same RNN-like context embedding abilities, and made BERT one of the most successfull NLP models in recent times. 
At the end of this part, participants are aware to how modern Deep Learning has completely replaced the old distributional language models.

A good chunk of this lecture series is dedicated to information extraction, which happens to be the author's favorite speciality:
We will cover the extraction of document summaries, and briefly discuss how modern deep learning methods can even generate new text (summaries).
Then we take a look at keyword extraction techniques, the arguably most basic information extraction technique in this section.
While possibly appearing trivial in comparison, keyword extraction is universally useful in a great many aspects of everyday text mining work.
Participants will encounter the fundamental text sequence tagging tasks: Parts-of-Speech tagging, (phrasal) chunking and Named Entity Recognition.
On the statistics side, we look at how probabilistic sequence models (HMMs, MEMMs, and CRFs) can be applied to label text for these tasks.
While modern LSTMs do no longer need to rely on the Markov assumption, these earlier models still form a solid baseline in the repertoire of any text miner.
Last but not least, CRFs still are used as the last layer of deep learning models for these fundamental tasks (PoS tagging, chunking, NER).
		
Finally, we will have a look at the "master-piece" of natural language processing, namely learning the grammatical structure of language;
That is, analyzing the syntactic structure of a sentence.
The resulting "parse trees" provide NLPers with syntactic and semantic relationships of the words in a sentence.
We will learn the differences between constituency (aka. phrase-structure) and dependency grammars, and take a closer look at the inner workings of a linear, transition-based, arc-standard, shift-reduce, greedy dependency parser model.

By the end, this class will have accompanied participants across the entire "journey" from simple statistical classifiers and the basics of search engines all the way to today's most sophisticated natural language understanding techniques.
Along all statges worked out (Jupyter) notebooks in Python should help you understand how all these techniques can be applied, thereby connecting theory to practice.

(c) Copyright 2014-2019. Florian Leitner. All rights reserved.
This material is distributed under the [Creative Commons BY-NC license](https://creativecommons.org/licenses/by-nc/4.0/).
