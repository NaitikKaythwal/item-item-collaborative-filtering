# Item-Item-collaborative-filtering algorithm
Item-Item collaborative filtering is one of the two recommender algorithms used to predict the user-ratings for the given movies, with the other one being user-user collaborative filtering. 

## Overview
The given algorithm uses a training data comprising of a small subset of the Netflix dataset consisting of movie ratings for 35 movies from 2.5K users and predict the user ratings for those movies located in the testing data. The algorithm first generates similarities between different movies using the user-ratings for the movies with the help of cosine similarity which calculates the similartiy between 2 movies on a scale of 0-1, 1 being the most similar. 
Using the similarity values, the algorithm predict the ratingsfor a particular movie based on the neighborhood of similar movies and uses K-nearest neighbors algorithm. For this given algorithm, I used different neighboorhood sizes of 5, 15 and 25 movies and calculate the mean-squared error for the algorithm in each case. Further, if there's a missing value and there's no ratings for the movie by the given user within the neighborhood of similar movies, the algorithm predicts the average ratings from all the users for the movie. 

The ratings-train.txt contains the training data and ratings-test.txt contains the testing data. The format of each line in these files is Movie-id, User-id, rating. That is, each line specifies a rating given by a user for a specific movie.
