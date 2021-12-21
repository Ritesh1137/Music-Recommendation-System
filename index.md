## Music Recommendation System - Final Project AAI 627 - Data Acquisition and Processing I: Big Data

This repo is being constructed to serve as a guide to building recommendation systems. If you want to know [what I learnt from the project, click here](https://github.com/MoronSlayer/Music-Recommendation-System/blob/main/628_final_proj_Prashant_Ritesh.pdf)

How does YouTube know what video you might want to watch next? How does the App Store pick an app just for you? Magic? No, in both cases, an ML-based recommendation model determines how similar videos and apps are to other things you like and then serves up a recommendation.
Generally, recommendation systems are built using one of two strategies:
#### content-based filtering :
 Content-based filtering uses item features to recommend other items similar to what the user likes, based on their previous actions or explicit feedback.
#### collaborative-based filtering : 
To address some of the limitations of content-based filtering, collaborative filtering uses similarities between users and items simultaneously to provide recommendations. This allows for serendipitous recommendations; that is, collaborative filtering models can recommend an item to user A based on the interests of a similar user B. Furthermore, the embeddings can be learned automatically, without relying on hand-engineering of features. 
[Neighborhood methods and Latent Factor Methods](https://www.asc.ohio-state.edu/statistics/dmsl//Koren_2009.pdf) are two widely used collaborative based filtering methods.

### The data used to build the music recommendation system has the following stats 

Training Data
 - 249K users 
 - 296K items 
 - 62M ratings scores
 
Test Data
 - 100K test users, 6 tracks per user
 - Test user in the training user set

The Music data is stored in a heirarchial structure as : 
Track -> Artist -> Album -> Genre 1 , Genre 2 ..... Genre K

#### Data format 
In the training data, the format given is:

- user 1 : item id : ratings , user 2 : item id : ratings .... user m : item id : ratings

- Here, each user has rated x number of items ( which correpond to either track id, album id , artist id or genre id ) and the rating for each one of those items. 

In the test data, the format given is: 

- user 1 -- track id - rating , user 2 -- track id - rating .... user n -- track id - rating

- Here, each user is given 6 tracks of which predictions are to be made to check which 3 tracks will the user will like and the 3 tracks he'll dislike. The objective of the system is to predict each user's ratings for their 6 given tracks. 

-The data is attached to the repo for further clarity.













### Bibliography :
[AnalyticsIndiamag](https://analyticsindiamag.com/collaborative-filtering-vs-content-based-filtering-for-recommender-systems/)<br />  \
[Google_Developers](https://developers.google.com/machine-learning/recommendation)
