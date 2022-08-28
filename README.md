# Recommendation-Systems

A recommender system, or a recommendation system (sometimes replacing 'system' with a synonym such as platform or engine), is a subclass of information filtering system that provide suggestions for items that are most pertinent to a particular user. Typically, the suggestions refer to various decision-making processes, such as what product to purchase, what music to listen to, or what online news to read. Recommender systems are particularly useful when an individual needs to choose an item from a potentially overwhelming number of items that a service may offer.

Recommender systems are used in a variety of areas, with commonly recognised examples taking the form of playlist generators for video and music services, product recommenders for online stores, or content recommenders for social media platforms and open web content recommenders.


## Collaborative Filtering
![Recommender-System-Collaborative-Filtering1-i2tutorials](https://user-images.githubusercontent.com/88277713/187086651-12d4e99c-9825-4599-88d7-b55aaa255bbf.jpg)

Collaborative Filtering: The assumption of this approach is that people who have liked an item in the past will also like the same in future. This approach builds a model based on the past behaviour of users. The user behaviour may include previously watched videos, purchased items, given ratings on items. In this way, the model finds an association between the users and the items. The model is then used to predict the item or a rating for the item in which the user may be interested. Singular value decomposition is used as a collaborative filtering approach in recommender systems. 

## Techniques

### Singular Value Decomposition

The Singular Value Decomposition (SVD), a method from linear algebra that has been generally used as a dimensionality reduction technique in machine learning. SVD is a matrix factorisation technique, which reduces the number of features of a dataset by reducing the space dimension from N-dimension to K-dimension (where K<N). In the context of the recommender system, the SVD is used as a collaborative filtering technique. It uses a matrix structure where each row represents a user, and each column represents an item. The elements of this matrix are the ratings that are given to items by users.

## Collaborative Filtering Movie Recommender System with SVD +100 K MovieLens Dataset
Access to Project

![1](https://user-images.githubusercontent.com/88277713/187087517-452154c3-a6e3-4955-a8b8-418835bba899.PNG)

![2](https://user-images.githubusercontent.com/88277713/187087741-6545f4b9-a001-4413-a17d-83c3f0b19126.PNG)



This is an implementation of singular value decomposition (SVD) based on collaborative filtering in the task of movie recommendation. This task is implemented in Python. For simplicity, the MovieLens 100k  Dataset has been used. This dataset has been chosen because it does not require any preprocessing as the main focus of this project  is on SVD and recommender systems.
