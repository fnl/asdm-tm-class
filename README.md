Statistical Text Mining in Python
=================================

This repo contains the PDF slides, Jupyter notebooks, corpora, and some software for a course on statistical [Text Mining](http://fnl.es/an-introduction-to-statistical-text-mining.html), part of the [Advanced Statistics and Data Mining Summer School](http://www.dia.fi.upm.es/ASDM) in Madrid (2018).

The two main differences to the actual class are (a) that the animations that are used to explain more complex algorithms/slides (similarity hashing, dependency parsing, etc.) are necessarily missing and (b) you obviously don't get my in-depth explanations and discussions of the slides you'd enjoy when visiting the class.
But this material should make it easier for you to follow the class, provide you with a good reference material for various text mining and language processing techniques, or simply help you to decide if this class indeed "is for you."

Apart from the full [Jupyter](http://jupyter.org/) stack with Python **3.x**, running the notebooks requires a working installation of [NLTK](http://www.nltk.org/), version 3.x (i.e., the latest stable release): `pip install nltk` or via installing the Continuum Analytics [Anaconda](http://continuum.io/downloads) Python distribution: `conda install nltk` .
Similary, you should have [`gensim`](http://radimrehurek.com/gensim/index.html) installed, which is probably the other core text mining tool that you can find in the Python world; Here at least we will be making heavy use of both.

To view the notebooks online, you can access them via the [Jupyter notebook viewer](https://nbviewer.jupyter.org/), by using the Git URLs in this repository, or installing a [browser extension](https://jiffyclub.github.io/open-in-nbviewer/) for Firefox, Chrome, or Safari that opens the GitHub page in the viewer format.
In general, simply clone or fork or download this repo to grab your own version of the course material.

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
* [`pytextrank`](https://github.com/ceteri/pytextrank)
* [`keras`](https://keras.io/)

Keras is only used to demonstrate how to plug word embeddings (representation learning) into a deep learning framework ([Keras](https://keras.io/)), and then run a text classification task with a Convolutional Neuronal Network (CNN) model.
(Obviously, those interested in deep learning should have visited the excellent course on neural networks (C05) the week before, as well as probably C01, C04, and C07, and C12, which are all about statistical learning techniques commonly used in text mining and NLP.)
And, there will be a quick glance at some of the [Stanford CoreNLP](https://stanfordnlp.github.io/CoreNLP/) tools, so having Java installed is necessary to run those examples.

Lecture Overview
----------------

The introduction mostly covers basic text mining: inverted indices, word vectors, TF-IDF weighting, document classification, and document similarity hashing (Locality Sensitive min-Hashing, LSH).
This day should give you all the basic tools to classify text and build your own text categorization systems.
Hopefully, this day should leave you with an early "aha" effect of what text mining "can do for you".
Right in the beginning, we will also spend some time to familiarize you with the most important concept in machine learning: model evaluation. In particular, we will look at ways of evaluating the performance of text mining models.

As the next leg, we take a look at some common unsupervised techniques to work with text.
The tools learned today are particularly useful to prepare your data and to apply text mining even if you cannot generate annotated datasets to train your classifiers.
In particular, we will cover graph processing ("PageRank") and document clustering techniques.
This day introduces sentence segmentation and text summarization tools, and looks into Latent Semantic Indexing and Latent Dirichlet Allocation-based clustering.

The program then dives into the most important fundamental concept of text mining and natural language understanding for machines: Representation learning.
You will learn what word embeddings are, where they "came from", how the most common (semi-) predictive models work (word2vec, Glove, FastText), and how to extend word embeddings to sentences, paragraphs, and documents.
To provide some context, representation learning forms the stepping stone to deep learning in natural language processing.

A large chunk of this lecture series is all dedicated to information extraction: We will start with some basics, looking at collocations, idioms, and keyword extraction techniques; While maybe seeming trivial, these techniques are used surprisingly often in everyday text mining work.
We will encounter some of the most common language processing concepts today: After the collocations, we discuss what the Parts-of-Speech are, and conclude with phrasal chunks and named entities; On that path, you will be introduced to word morphology and lemmas, as well.
On the statistics side, we quickly remind you of the Markov property, and then look at how probabilistic sequence models (HMMs, MEMMs, and CRFs) can be applied to label text.
While modern Recurrent and Recursive Neural Networks do no longer need to rely on the Markov assumption, these simpler models still form a solid baseline in your repertoire as text miner, not the least because they can be trained with very little data (compared to data-hungry deep learning techniques).
		
Finally, we will have a look at the "master-piece" in text mining, namely *parsing* natural language, that is graphing the syntactic structure of the words in a sentence.
The resulting "parse tree" provides us with semantic information about the relationships of the words.
We will learn the differences between constituency (aka. phrase-structure) and dependency grammars and take a closer look at a linear, transition-based, arc-standard, shift-reduce, greedy dependency parser model.

(c) Copyright 2014-2018. Florian Leitner. All rights reserved.
This material is distributed under the [Creative Commons BY-NC license](https://creativecommons.org/licenses/by-nc/4.0/).
