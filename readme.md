## Task

To make a search engine using a given dataset of products

## Approach

As the dataset of products given is unlabelled containing only one column having the name of the products.

[Given Dataset](https://github.com/rishabhdhenkawat/productSearchEngine/blob/main/dataset/products%20-%20products.csv)

Hence to make the search more accurate and semantic 4 scrapers are made to collect descriptions of products using Bing Search and use cases of each product is collected.

[DATASET WITH DESCRIPTION](https://github.com/rishabhdhenkawat/productSearchEngine/blob/main/dataset/final%20main.csv)

[Scrapers Code](https://github.com/rishabhdhenkawat/productSearchEngine/tree/main/scapers)

![final search engine flow](![final search engine flow](https://user-images.githubusercontent.com/44580998/125502873-35d727d3-f9de-4b7e-98e6-8897ad234eff.png))
## Algorithms Used

###### The final results are given by using several algorithms.

### Kmeans Clustering with TF-IDF vectorizer

Word embeddings of textual description products are converted using TF-IDF Vectorizer and then clustering is done using Kmeans with K=10000 (selected after using Elbow method).

[Traning Code](https://github.com/rishabhdhenkawat/productSearchEngine/blob/main/training%20codes/Kmens%20clustering%20with%20TF%20IDF%20Vectorizer.ipynb)

nearest cluster data points to the given query are selected as results.

### Kmeans Clustering with Google pre-trained embeddings

As the dataset contains Hindi terms also so word embeddings with Wikipedia and news data are selected as pre-trained vectors.

clustering is done using Kmeans with K=10000 (selected after using the Elbow method).

[Traning Code](https://github.com/rishabhdhenkawat/productSearchEngine/blob/main/training%20codes/Kmeans%20clustering%20with%20google%20pretrained%20vectors.ipynb)

nearest cluster data points to the given query are selected as results.

### Content-based search engine using Word Embeddings

average Word2Vec and TF-IDF Word2Vec are be used to build the engine.

A simple neural network model with a single hidden layer is used. It predicted the adjacent words for each and every word in the sentence or corpus. The weights that are learned by the hidden layer of the model and the same can be used as word embeddings.

[Traning Code](https://github.com/rishabhdhenkawat/productSearchEngine/blob/main/training%20codes/Content%20Basded%20Search%20Engine%20with%20AvgWord2Vec%20and%20TfIDFWord2Vec%20.ipynb)


#### average Word2Vec

Sum all the vectors and divide the same by a total number of words in the description
  
![1_yZtMrZlG4SeemjHQIAtffg](https://user-images.githubusercontent.com/44580998/125311531-1b037680-e351-11eb-8542-ecf389365c29.png)


#### TF-IDF Word2Vec

![1_WvyAn4dQq3rxvPot8-dvsg](https://user-images.githubusercontent.com/44580998/125311541-1b9c0d00-e351-11eb-8162-47166c969f56.png)

###### The final result is given by calculating cosine similarity between the query and the input dataset

### Custom CNN 

Unalabelled product data have been categorized using the clusters gven by Kmeans and convolution neural nets have been used to search the best fit product as the given query

[Kaggle training code](https://www.kaggle.com/rishabhdhenawat/cnn-search-engine)

[Traning Code](https://github.com/rishabhdhenkawat/productSearchEngine/blob/main/training%20codes/cnn%20search%20engine.ipynb)


##### Custom CNN Architecture    
![cnn arch](https://user-images.githubusercontent.com/44580998/125443007-1178f9c6-885a-4688-8472-35252bd93188.JPG)
  
  
##### Custom CNN Taining Epochs and Accuracy
![Custom CNN Taining Epochs and Accuracy](https://user-images.githubusercontent.com/44580998/125499525-3ecdfc42-3e67-4a1c-8d9d-016ab7662e45.JPG)

 

###### Training on LSTM and GRU traning is also done but accuracy was not upto the mark for the models
[Kaggle code](https://www.kaggle.com/rishabhdhenawat/lstm-gru) 


## Steps to run the code

- Clone this repo 
- Open the cloned directory
- run pip install  -r requirements.txt
- Download the folder from the given [link](https://drive.google.com/drive/folders/1-En9EiHroavDjU7APcfS4IUurCuhIhPY?usp=sharing)
- Run "final search engine.ipnyb" to explore all the algorithms and search the queries



