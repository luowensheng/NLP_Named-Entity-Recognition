<p align="center">
    <a href="https://github.com/luowensheng"><img src="https://i.ibb.co/0FmPqfm/logo1a.png"></a>
</p>

<h3 align="center">Natural Language Processing:</h3>
<h1 align="center">Named Entity Recognition
</h1>
<p align="center">
    <a href="https://jupyter.org/"><img src="https://img.shields.io/badge/Made with-Jupyter Notebook-Orange.svg"></a>
    <a href="https://github.com/luowensheng/NLP_Named-Entity-Recognition/pulse"><img src="https://img.shields.io/badge/Maintained%3F-yes-green.svg"></a>
    <a href="https://github.com/luowensheng"><img src="https://badges.frapsoft.com/os/v2/open-source.svg?v=103"></a>
</p>

<p align="center">
  <a href="#Introduction">Introduction</a> •
  <a href="#Tasks">Tasks</a> •
  <a href="#Results">Results</a> •
  <a href="#Comparisons">Comparisons</a> •
  <a href="#Questions">Questions</a>
</p>

___

<br>

# Introduction
[(Back to top :arrow_up_small:)](#Named-Entity-Recognition)

**Named-entity recognition (NER)** (also known as entity identification, entity chunking and entity extraction) is a sub-task of information extraction that seeks to locate and classify named entities in text into pre-defined categories such as the names of persons, organizations, locations, expressions of times, quantities, monetary values, percentages, etc.

Our dataset consists of many labels one of which is the overwhelming majority. In machine learning, we called this an unbalanced dataset.

We have to train a Chinese NER model using ```sklearn-crfsuite``` module and evaluate its performance. Character based Chinese NER dataset in ```json``` format will be given. Then we try to improve model performance using suggested methods and compare the results.

<h3 align="center"><b>Procedure:</h3></b>
<p align="center">
<img src="https://i.ibb.co/k8PtKzp/1.jpg" width="400"></a>
</p>

## **sklearn-crfsuite**
* **Feature Engineering**

    <img src="https://i.ibb.co/qMM8DGY/2.jpg" alt="2" border="0"></a>

* **Assign feature as training data**

    <img src="https://i.ibb.co/61ctmbs/3.jpg" alt="3" border="0"></a>

* **Training**

    <img src="https://i.ibb.co/4f5j1Hk/4.jpg" alt="4" border="0"></a>

* **Evaluation**

    <img src="https://i.ibb.co/LZwJ8Dn/5.jpg" alt="5" border="0"></a>
    <br>
    <img src="https://i.ibb.co/m8H3qPd/6.jpg" alt="6" border="0"></a>
    <br>
    <br>
    <img src="https://i.ibb.co/zfBBnpg/7.jpg" alt="7" border="0"></a>
    <br>
    <br>
    <img src="https://i.ibb.co/7gmm0WW/8.jpg" alt="8" border="0"></a>


## **Dataset**

<img src="https://i.ibb.co/zftFNfQ/9.jpg" alt="9" border="0"></a>
<br>
<img src="https://i.ibb.co/CmwwCLx/10.jpg" alt="10" border="0"></a>
<br>
<img src="https://i.ibb.co/pPf9bpW/11.jpg" alt="11" border="0"></a>

* ```train_char.json```
* ```validation_char.json```
* ```test_char.json```
>[token, pos, neLabel]

## **Word2Vec**
* Pre-trained model:
    * Trained from 中央社CNA.
    * File: ```cna.word2vec.bin```
    * Dimension: 300.
* Self-trained model:
    * ```Word2Vec model``` was already trained.
    * Training from the Chinese NER data given.
    * File: ```ch.300.bin```
    * Dimension: 300
* [Gensim documentation](https://radimrehurek.com/gensim/models/keyedvectors.html)

    <img src="https://i.ibb.co/SRJqj7t/12.jpg" alt="12" border="0"></a>

# Tasks
[(Back to top :arrow_up_small:)](#Named-Entity-Recognition)

- [x] Train a Chinese NER model using ```sklearn-crfsuite```
module and evaluate its performance. Character-based
Chinese NER dataset in json format was given.
- [x] Improve model performance using suggested
methods and compare the results.


# Results
[(Back to top :arrow_up_small:)](#Named-Entity-Recognition)

### **Method 1**
:clock1: Training time: 3min 47s

<img src="https://i.ibb.co/bL75Ps9/13.jpg" alt="13" border="0"></a>

### **Method 2**
:clock1: Training time = 4 min 46s

<img src="https://i.ibb.co/8nktK2L/14.jpg" alt="14" border="0"></a>

### **Method 3**
:clock1: Training time = 1h 30 min

<img src="https://i.ibb.co/fCtY4wX/15.jpg" alt="15" border="0"></a>

### **Method 4**
:clock1: Training time= 5 min 27 s

<img src="https://i.ibb.co/j5FWxRS/16.jpg" alt="16" border="0"></a>


# Comparisons
[(Back to top :arrow_up_small:)](#Named-Entity-Recognition)

| Word Based | Character Based |
| :--: | :--: |
| <img src="https://i.ibb.co/qg1KCC7/17.jpg" alt="17" border="0">| <img src="https://i.ibb.co/GcxWqmf/18.jpg" alt="18" border="0"> |

|        | The percentage of characters that are not in the Dict for word based | The percentage of characters that are not in the Dict for character based |
| :--- | :--: | :--: |
| Cna.word2vec.bin | 0.2817314746881878 | 0.17794290183809153 |
| ch.300.bin | 0.5798548094373865 | 0.5001955416503715 |
<br>
<br>

**Word-based** gives better results because of the fact that some words can have many characters. It makes it easier to get better results, whereas **character-based** takes more to get higher results.

The dictionary for the character-based method provided very little improvement but it provided much more improvement for word based due to its word-based nature. It allows to the for more accurate results when a Dictionary is used.

The ```Word2vec``` models that we were provided were missing a lot of characters which hinders the performance of the model. Training also takes way too long which makes testing different ideas much harder.

# Questions
Submit your questions and bug reports [here](https://github.com/luowensheng/Natural-Language-Processing-Grammatical-Error-Correction-/issues).


<br>
<p align="center">
    <img src="https://forthebadge.com/images/badges/built-by-developers.svg"> <img src="https://forthebadge.com/images/badges/uses-git.svg"></a>
<p align="center">  
  <sub>© luowensheng.
  </a></p>


