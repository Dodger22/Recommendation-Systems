# Recommendation-Systems

A recommender system, or a recommendation system (sometimes replacing 'system' with a synonym such as platform or engine), is a subclass of information filtering system that provide suggestions for items that are most pertinent to a particular user. Typically, the suggestions refer to various decision-making processes, such as what product to purchase, what music to listen to, or what online news to read. Recommender systems are particularly useful when an individual needs to choose an item from a potentially overwhelming number of items that a service may offer.

Recommender systems are used in a variety of areas, with commonly recognised examples taking the form of playlist generators for video and music services, product recommenders for online stores, or content recommenders for social media platforms and open web content recommenders.

### Projects

1- [Collaborative Filtering Movie Recommender System with SVD +100 K MovieLens Dataset](https://github.com/mirzaozeer/Recommendation-Systems-Collaborative-Filtering#collaborative-filtering-movie-recommender-system-with-svd-100-k-movielens-dataset)

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




## Collaborative Filtering Movie Recommender System with SVD +100 K MovieLens Dataset
[Access to Project](https://github.com/Dodger22/Recommendation-Systems/blob/main/Collaborative_Filtering_Movie_Recommender_System_with_SVD.ipynb)

This is an implementation of singular value decomposition (SVD) based on collaborative filtering in the task of movie recommendation. This task is implemented in Python. For simplicity, the MovieLens 100k  Dataset has been used. This dataset has been chosen because it does not require any preprocessing as the main focus of this project  is on SVD and recommender systems.

![1](https://user-images.githubusercontent.com/88277713/187087517-452154c3-a6e3-4955-a8b8-418835bba899.PNG)

![2](https://user-images.githubusercontent.com/88277713/187087741-6545f4b9-a001-4413-a17d-83c3f0b19126.PNG)



