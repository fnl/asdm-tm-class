Statistical Text Mining in Python
=================================

*IMPORTANT*: The current notebooks are *not* yet in sync with the slides (for 2017) and are still from last year's (2016) course!

This repo contains the PDF slides, Jupyter notebooks, corpora, and some software for a course on statistical [Text Mining](http://fnl.es/an-introduction-to-statistical-text-mining.html), part of the [Advanced Statistics and Data Mining Summer School](http://www.dia.fi.upm.es/ASDM) in Madrid.

The two main differences to the actual class are (a) that the animations that are used to explain more complex algos/slides (similarity hashing, dependency parsing, etc.) are necessarily missing and (b) you obviously don't get my in-depth explanations and discussions of the slides you'd enjoy when visiting the class.
But this material should make it easier for you to follow the class, provide you with a good reference material for various text mining and language processing techniques, or simply help you to decide if this class indeed "is for you."

Apart from the full [Jupyter](http://jupyter.org/) stack with Python **3.x**, running the notebooks requires a working installation of [NLTK](http://www.nltk.org/), version 3.x (i.e., the latest stable release): `pip install nltk` or via installing the Continuum Analytics [Anaconda](http://continuum.io/downloads) Python distribution: `conda install nltk` .
Other libraries to install in the same manner include [gensim](http://radimrehurek.com/gensim/index.html), [SciKit-Learn](http://scikit-learn.org/stable/), and [SpaCy](https://spacy.io/).

To view the notebooks online, you can access them via the Jupyter notebook viewer, by following the links in this README.
To view the slides online, please follow the links in this README to see them on GitHub.
Otherwise, simply clone or fork this repo to grab your own version of the material.

Introduction
------------

There are three introductory notebooks that students are encouraged to study before visiting the class:

1. There is a quick notebook to familiarize yourself with [Jupyter notebooks](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Jupyter.ipynb) in general.
1. Check if your Python skills are in shape: You should understand [most of this](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Python.ipynb), otherwise you might want to first brush up a bit on your Python expertise.
1. Finally, a quick introduction to [the basics of NLTK and NumPy](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/NLTK%20and%20NumPy.ipynb) that is recommended for all but experts familiar with the two libraries.

Day 1: Text Mining
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%201.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%201.ipynb)

Day one mostly covers basic text mining: inverted indices, word vectors, TF-IDF weighting, and document similiarity hashing (Locality Sensitive min-Hashing, LSH).
This day should give you all the basic tools to classify text and build your own text categorization systems.
Hopefully, this day should leave you with an early "aha" effect of what text mining "can do for you".

Day 2: Unsupervised Methods
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%202.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%202.ipynb)

On day two, we take a look at some common unsupervised techniques to work with text.
The tools learned today are particularly useful to prepare your data and to apply text mining even if you cannot generate annotated datasets to train your classifiers.
In particular, we will cover graph processing ("PageRank") and document clustering techniques.
This day introduces sentence segmentation and text summarization tools, and looks into Latent Semantic Indexing and Latent Dirichlet Allocation-based clustering.

Day 3: Representation Learning
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%203.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%203.ipynb)

The program for day three dives into the most important fundamental concept of text mining and natural language understanding for machines: Represenation learning.
You will learn what word embeddings are, where they "came from", how the most common (semi-) predictive models work (word2vec, Glove, FastText), and how to extend word embeddings to sentences, paragraphs, and documents.
To provide some context, representation learning forms the stepping stone to deep learning in natural language processing.

Day 4: Information Extraction
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%204.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%204.ipynb)

Day four is all dedicated to information extraction: We will start with some basics, looking at collocations, idioms, and keyword extraction techniques; While maybe seeming trivial, these techniques are used surprisingly often in everyday text mining work.
We will encounter some of the most common language processing concepts today: After the collocations, we discuss what the Parts-of-Speech are, and conclude with phrasal chunks and named entities; On that path, you will be introduced to word morphology and lemmas, as well.
On the statistics side, we quickly remind you of the Markov property, and then look at how probabilitistic sequence models (HMMs, MEMMs, and CRFs) can be applied to label text.
While modern Recurrent and Recursive Neural Networks do no longer need to rely on the Markov assumption, these smipler models still form a solid baseline in your reportoire as text miner, not the least because they can be trained with very little data (compared to data-hungry deep learning techniques).
		
Day 5
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%205.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%205.ipynb)

The last day will spend some time to familiarize you with the most important concept in machine learning: model evaluation, and how to measure the performance of text mining models.
Finally, we will have a look at the "master-piece" in text mining, namely *parsing* natural language, that is detecting the syntacic structure of sentences to derive semantic information thereof.
We will learn the differences between constituency (aka. phrase-structure) and dependency grammars and take a closer look at a linear, transition-based, arc-standard, shift-reduce, greedy dependency parser model.
The remainder of the last day we then will see how all these techniques can be combined to extract "events" (relationships) from text.

(c) 2014-2017. Florian Leitner. All rights reserved.
This material is distributed under the [Creative Commons BY-NC license](https://creativecommons.org/licenses/by-nc/4.0/).
