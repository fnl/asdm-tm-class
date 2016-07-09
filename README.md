Statistical Text Mining in Python
=================================

This repo contains the PDF slides, Jupyter notebooks, corpora, and [StanfordNLP JARs](http://nlp.stanford.edu/software/) for a course on statistical [Text Mining] (http://fnl.es/an-introdcution-to-statistical-text-mining.html), part of the [Advanced Statistics and Data Mining Summer School] (http://www.dia.fi.upm.es/ASDM) in Madrid.

The two main differences to the actual class are (a) that the animations that are used to explain more complex algos (similarity hashing, parsing, etc.) are necessarily missing and (b) you obviously don't get my in-depth explanations and discussions of the slides you'd enjoy when visiting the class.
But this material should make it easier for you to follow the class, provide you with a good reference material for various text mining and language processing techniques, or simply help you to decide if this class indeed "is for you."

Apart from the full [Jupyter] (http://jupyter.org/) stack with Python **3.x**, running the notebooks requires a working installation of [NLTK] (http://www.nltk.org/), version 3.x (i.e., the latest stable release): `pip install nltk` or via installing the Continuum Analytics [Anaconda] (http://continuum.io/downloads) Python distribution: `conda install nltk` .
Other libraries to install in the same manner include [gensim] (http://radimrehurek.com/gensim/index.html), [SciKit-Learn] (http://scikit-learn.org/stable/), and [SpaCy] (https://spacy.io/).

To view the notebooks online, you can access them via the Jupyter notebook viewer, by following the links in this README.
To view the slides online, please follow the links in this README to see them on GitHub.
Otherwise, simply clone or fork this repo to grab your own version of the material.

Introduction
------------

There are three introductory notebooks that students are encouraged to study before visiting the class:

1. There is a quick notebook to familiarize yourself with [Jupyter notebooks] (http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Jupyter.ipynb) in general.
1. Check if your Python skills are in shape: You should understand [most of this] (http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Python.ipynb), otherwise you might want to first brush up a bit on your Python expertise.
1. Finally, a quick introduction to [the basics of NLTK and NumPy] (http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/NLTK%20and%20NumPy.ipynb) that is recommended for all but experts familiar with the two libraries.

Day 1
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%201.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%201.ipynb)

Day one mostly covers the basics: inverted indices, Bayesian statistics, tokenization, and sentence segmentation.

Day 2
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%202.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%202.ipynb)

The first thing to understand is how to expand Bayesian statistics to build language models, Markov chains, and then we dive into the first ("neural") word embedding technique using a simple perceptron.
This part also compares extrinsic to intrinsic evaluation, and look at entropy and perplexity.
Day two also covers an [additional notebook] (http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%202%20-%20Spelling%20Correction%20Norvig.ipynb) discussing the implementation of a spelling correction system as suggested by Peter Norvig.

Day 3
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%203.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%203.ipynb)

The course finally starts to speed up and the day covers some of the most critical parts: string similarity, Locality Sensitive Hashing, TF-IDF, and Latent Semantic Indexing.
This material provides you with everything needed to build semantic search-engines.
In closing, we also quickly look at naïve Bayes classification, as an introduction to tomorrow's more advanced coverage of this topic.
Day three covers an [additional notebook] (http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%203%20-%20Spelling%20Correction%20LSH.ipynb) discussing how to speed up the implementation of a spelling correction system by using an LSH bi-gram dictionary.

Day 4
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%204.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%204.ipynb)

Day four is all dedicated to text classification: after yesterday's quick rehearsal of naïve Bayes, we study how the maximum entropy (MaxEnt)/multinomial logistic regression classifier works in-depth.
This preparation should help you understand both the more advanced classifiers like MaxEnt and conditional Markov models (MEMM, CRF - see Day 5) or neural networks (part of another ASDM course).
After that, we explore our first probabilistic graphical model, Latent Dirichlet Allocation (LDA), and close the day with evaluation techniques for classifiers, in particular comparing ROC to PR curves and discussing why you normally should always prefer AUC PR over AUC ROC.
		
Day 5
-----

* [Presentation](https://github.com/fnl/asdm-tm-class/blob/master/Day%205.pdf)
* [Notebook](http://nbviewer.jupyter.org/github/fnl/asdm-tm-class/blob/master/Day%205.ipynb)

Finally, after building up all the necessary basics, the "advanced" class today should be a breeze and in the ideal case leave you with some "aha-effect".
We will be studying dynamic models (sequence tagging) - in particular, hidden Markov models, MaxEnt Markov models, and [Markov] conditional random fields - and how transition-based shift-reduce parsers annotate dependencies on token sequences.

(c) 2016. Florian Leitner. All rights reserved.
This material is distributed under the [Creative Commons BY-NC license](https://creativecommons.org/licenses/by-nc/4.0/).
