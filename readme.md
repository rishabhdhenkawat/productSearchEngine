## Task

To make a search engine using a given dataset of products

## Approach

As the dataset of products given is unlabelled containing only one column having the name of the products.

<Given Dataset>

Hence to make the search more accurate and semantic 4 scrapers are made to collect descriptions of products using Bing Search and use cases of each product is collected.
<DATASET WITH DESCRIPTION>

<Scrapers Code>

## Algorithms Used

The final results are given by using several algorithms.

### Kmeans Clustering with TF-IDF vectorizer

Word embeddings of textual description products are converted using TF-IDF Vectorizer and then clustering is done using Kmeans with K=10000 (selected after using Elbow method).

<Traing Code>

nearest cluster data points to the given query are selected as results.

### Kmeans Clustering with Google pre-trained embeddings

As the dataset contains Hindi terms also so word embeddings with Wikipedia and news data are selected as pre-trained vectors.

clustering is done using Kmeans with K=10000 (selected after using the Elbow method).

<Traing Code>

nearest cluster data points to the given query are selected as results.

### Content-based search engine using Word Embeddings

average Word2Vec and TF-IDF Word2Vec are be used to build the engine.

A simple neural network model with a single hidden layer is used. It predicted the adjacent words for each and every word in the sentence or corpus. The weights that are learned by the hidden layer of the model and the same can be used as word embeddings.

<Training Code>

#### average Word2Vec

Sum all the vectors and divide the same by a total number of words in the description

<pic>


#### TF-IDF Word2Vec

<pic>


The final result is given by calculating cosine similarity between the query and the input dataset



## Steps to run the code

Clone this repo 
Open the cloned directory
run pip install  -r requirements.txt
Download the trained weights and dataset from the given link
Run main. ipnyb to explore all the algorithms and search the queries



