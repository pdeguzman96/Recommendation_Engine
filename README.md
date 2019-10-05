# Build a Recommendation Engine with IBM

This project is part of the Data Science Nanodegree by [Udacity](https://eu.udacity.com/). It features an important collaboration with IBM, the provider of the dataset. The aim is to develop a recommendation engine and suggest new articles to the [IBM Watson Community](https://dataplatform.cloud.ibm.com/community?context=wdp) users.

## Details

### Data
The data provided consists of...
1. `articles_community.csv`: which is a list of all of the articles, their names, and their descriptions on the IBM Watson platform
2. `user-item-interactions.csv`: this is essentially a log that keeps track of user_id's and article_id's whenever a user interacts with an article

### The Recommendation Engine
The recommendation consists of a few different moving parts...
1. Knowledge-Based recommendations: Recommends items based on popularity
2. Collaborative Filtering: Recommends itms based on similar users' interactions with most popular items
    - Similarity is determined by most common user-item interactions
    - most popular items was determined by knowledge-based popularity
3. Content-Based Filtering:  For a given user, recommends similar items based on items that the user has interacted with
    - Item similarity is based on euclidean distance between tf-idf vectorized descriptions of items
4. Matrix Factorization: Singular Value Decomposition (SVD) was performed on a training dataset and evaluated on a test dataset to predict whether a user would interact with an item.

## Conclusion
An optimal recommendation engine would most likely consist of a blend of some or all of the four recommendation systems outlined above. A great way to determine what works best would be to A/B test each engine against a benchmark using a metric like average interactions per view.

## Dependencies
- sklearn
- nltk
- pandas
- numpy
- progressbar2