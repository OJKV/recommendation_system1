# recommendation_system1
This project focuses on developing a recommendation system that provides personalized content recommendations to users based on their preferences and behavior. 


Data Preparation:
The script reads the recommendation data from a CSV file, which includes information about user ratings for different items.
Duplicate entries in the 'User ID' and 'Item ID' columns are dropped to ensure data integrity.
The remaining data is used to create a user-item matrix, where each cell represents the user's rating for a particular item. Missing values are filled with zeros.



Collaborative Filtering:
The script computes the item-item similarity matrix using cosine similarity.
A k-Nearest Neighbors (k-NN) model is fitted on the item similarity matrix to find similar items.
The collaborative filtering approach utilizes the k-NN model to recommend similar items to the ones already interacted with by the user.

Recommendation Functions:
The script defines the collaborative_filtering_recommendation function, which takes an item ID and the number of recommendations as input.
This function identifies similar items based on collaborative filtering using the k-NN model.
The hybrid_recommendation function is also defined to recommend items using a combination of collaborative filtering and content-based filtering.

Hybrid Recommendation:
The hybrid_recommendation function retrieves the items that the user has interacted with.
For each item, it finds similar items using collaborative filtering.
The function combines the recommendations from all the user's items and returns the top-N recommended items.

Testing the Recommendation System:
The script allows you to specify a user ID and the number of recommendations to generate.
The hybrid_recommendation function is called to obtain the recommended items for the given user.
The recommended items are then printed out.
By following these steps, the recommendation system utilizes collaborative filtering techniques to recommend similar items based on user-item interactions. The system takes into account the preferences of the user and provides personalized recommendations.
