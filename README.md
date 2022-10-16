# Recommendation-Systems

A recommender system, or a recommendation system (sometimes replacing 'system' with a synonym such as platform or engine), is a subclass of information filtering system that provide suggestions for items that are most pertinent to a particular user. Typically, the suggestions refer to various decision-making processes, such as what product to purchase, what music to listen to, or what online news to read. Recommender systems are particularly useful when an individual needs to choose an item from a potentially overwhelming number of items that a service may offer.

Recommender systems are used in a variety of areas, with commonly recognised examples taking the form of playlist generators for video and music services, product recommenders for online stores, or content recommenders for social media platforms and open web content recommenders.

### Projects

1- [Collaborative Filtering Movie Recommender System with SVD +100 K MovieLens Dataset](https://github.com/mirzaozeer/Recommendation-Systems-Collaborative-Filtering#collaborative-filtering-movie-recommender-system-with-svd-100-k-movielens-dataset)

2- [Neural Collaborative Filtering NeuMF model with Amazon Fashion Dataset](https://github.com/mirzaozeer/Recommendation-Systems-Collaborative-Filtering/blob/main/Collaborative_Filtering_NeuMF_Model_Amazon_Fashion_Dataset.ipynb)

3- [CONTENT BASED RECCOMENDATION SYSTEM (TF-IDF)](https://github.com/mirzaozeer/Recommendation-Systems-Models/blob/main/Content_Based_TF-IDF_Movie-Reccomendation.ipynb)

## Collaborative Filtering
![Recommender-System-Collaborative-Filtering1-i2tutorials](https://user-images.githubusercontent.com/88277713/187086651-12d4e99c-9825-4599-88d7-b55aaa255bbf.jpg)

Collaborative Filtering: The assumption of this approach is that people who have liked an item in the past will also like the same in future. This approach builds a model based on the past behaviour of users. The user behaviour may include previously watched videos, purchased items, given ratings on items. In this way, the model finds an association between the users and the items. The model is then used to predict the item or a rating for the item in which the user may be interested. Singular value decomposition is used as a collaborative filtering approach in recommender systems. 

## Techniques

### 1- Singular Value Decomposition

The Singular Value Decomposition (SVD), a method from linear algebra that has been generally used as a dimensionality reduction technique in machine learning. SVD is a matrix factorisation technique, which reduces the number of features of a dataset by reducing the space dimension from N-dimension to K-dimension (where K<N). In the context of the recommender system, the SVD is used as a collaborative filtering technique. It uses a matrix structure where each row represents a user, and each column represents an item. The elements of this matrix are the ratings that are given to items by users.

#### Matrix Factorization

![1 n-vTVJgQahPXRI09mMpKNA](https://user-images.githubusercontent.com/88277713/192288212-d0f19e4a-8bf2-4200-8813-9785190e3d92.png)
We have m users and n items. The goal of our recommendation system is to build an mxn matrix (called the utility matrix) which consists of the rating (or preference) for each user-item pair. Initially, this matrix is usually very sparse because we only have ratings for a limited number of user-item pairs.

Later,  our goal is to populate this matrix by finding similarities between users and items. 

m = Users
n = items

### 2- NeuMF (Neural Matrix Factorisation)

SVD model with MF,  simple multiplication of latent features (inner product), may not be sufficient to capture the complex structure of user interaction data.

This calls for designing a better, dedicated interaction function for modeling the latent feature interaction between users and items. 

Neural Collaborative Filtering (NCF) aims to solve this by: 

- Modeling user-item feature interaction through neural network architecture. It utilizes a Multi-Layer Perceptron(MLP) to learn user-item interactions. This is an upgrade over MF as MLP can learn any continuous function and has high level of nonlinearities(due to multiple layers) making it well endowed to learn user-item interaction function.

- Generalizing and expressing MF as a special case of NCF. As MF is highly successful in the recommendation domain, doing this will give more credence to NCF.

![1 Tqk7Q2q7wsr6MLF8Xl-emg](https://user-images.githubusercontent.com/88277713/193584199-0dda9a53-8ab3-4ca6-88b8-f0d5eb00bc55.png)

1- Input Layer binarise a sparse vector for a user and item identification where:
- Item (i): 1 means the user u has interacted with Item(i)
- User (u): To identify the user

2- Embedding layer is a fully connected layer that projects the sparse representation to a dense vector. The obtained user/item embeddings are the latent user/item vectors.

3- Neural CF layers use Multi-layered neural architecture to map the latent vectors to prediction scores.

4- The final output layer returns the predicted score by minimizing the pointwise loss/pairwise loss.


## 2-  Content Based 

![1 GKeESn8RruAbAUEm4k3_EQ](https://user-images.githubusercontent.com/88277713/196035689-b36fc741-2252-49d6-bc73-85ba1c03bc9a.png)

This type of filter does not involve other users if not ourselves. Based on what we like, the algorithm will simply pick items with similar content to recommend us. In this case there will be less diversity in the recommendations, but this will work either the user rates things or not

This model is easily scalable due to low amounts of data. Moreover, since, unlike other models, this does not need to compare with other users’ data, it can offer niche results specific to the current user.

## Techniques
![1 V9ac4hLVyms79jl65Ym_Bw](https://user-images.githubusercontent.com/88277713/196035970-bfb45404-d62f-41eb-9b45-e12d7df82e00.png)

### 1- TF-IDF

TF-IDF (term frequency-inverse document frequency) is a statistical measure that evaluates how relevant a word is to a document in a collection of documents.

This is done by multiplying two metrics: how many times a word appears in a document, and the inverse document frequency of the word across a set of documents.

It has many uses, most importantly in automated text analysis, and is very useful for scoring words in machine learning algorithms for Natural Language Processing (NLP).

The term frequency of a word in a document. There are several ways of calculating this frequency, with the simplest being a raw count of instances a word appears in a document. Then, there are ways to adjust the frequency, by length of a document, or by the raw frequency of the most frequent word in a document.
The inverse document frequency of the word across a set of documents. This means, how common or rare a word is in the entire document set. The closer it is to 0, the more common a word is. This metric can be calculated by taking the total number of documents, dividing it by the number of documents that contain a word, and calculating the logarithm.
So, if the word is very common and appears in many documents, this number will approach 0. Otherwise, it will approach 1.


