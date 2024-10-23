## Movie_recommendation System

# Creating a Recommender System to show personalized movie recommendations based on ratings given by a user and other users similar to them in order to improve user experience.

# Summary of Movie Recommendation System

1. **Loading and Preprocessing Movie Data:**
   - The **movies** dataset was loaded, and the **genres** column was split into individual genres for each movie.
   - Dummy variables for each genre were created, and the movies were grouped to represent genres in a binary format (1 for presence of the genre, 0 for absence).
   - The dataset was structured so that each movie had its corresponding genres in a format suitable for further analysis.

2. **Analyzing Genre Distribution:**
   - The unique genres in the dataset were extracted, and the most common genres were identified.
   - A bar plot was created to visualize the top 5 genres based on their frequency in the dataset.

3. **Processing Ratings Data:**
   - The **ratings** dataset, which contained combined user, movie, and rating information, was split into individual columns for user IDs, movie IDs, and ratings.
   - The unnecessary **timestamp** column was dropped, and the dataset was cleaned to focus only on user IDs, movie IDs, and ratings.

4. **Processing User Data:**
   - The **users** dataset was split into individual columns for user ID, gender, age, and other demographic information.
   - The gender column was encoded numerically (0 for male, 1 for female), and the age values were converted to integers.
   - The dataset was cleaned, with unnecessary columns removed.

5. **Merging Datasets:**
   - The **ratings**, **users**, and **movies** datasets were merged to form a comprehensive dataset that included user ratings for each movie, along with user demographics and movie genres.

6. **Top 5 Movies by Average Rating:**
   - The average rating for each movie was calculated, and the top 5 highest-rated movies were identified.
   - A horizontal bar chart was created to visualize the top 5 movies based on their average ratings.

7. **Top 5 Animation Movies:**
   - The dataset was filtered to include only movies categorized as "Animation."
   - The top 5 animation movies were identified based on their average ratings, and a horizontal bar chart was plotted to display these movies.

8. **User-Movie Matrix Creation:**
   - A user-movie matrix was created, where rows represented users, columns represented movies, and values represented the ratings each user gave to a specific movie.
   - Missing ratings were initially filled with zeros, and this matrix was prepared for further analysis.

9. **Collaborative Matrix Factorization:**
   - The matrix was decomposed using Collaborative Matrix Factorization (CMF) with Alternating Least Squares (ALS) to predict missing ratings.
   - The predicted ratings were used to fill in the missing entries in the user-movie matrix.

10. **Item-Item Similarity Matrix:**
   - A similarity matrix was computed based on the Pearson correlation between movies, helping identify how similar one movie is to another based on user ratings.
   - This matrix was used for item-item recommendations.

11. **Item-Based Movie Recommendation System:**
   - A function was implemented to recommend the top 5 movies similar to a given movie based on the item-item similarity matrix.
   - This allowed for movie recommendations based on the similarity of movies.

12. **User-User Similarity Matrix:**
   - A cosine similarity matrix was created for users based on their movie rating patterns.
   - This matrix helped identify users who had similar preferences.

13. **User-Based Recommendation System:**
   - A user-based recommendation function was created, which recommended movies that similar users had seen but the target user had not yet watched.
   - This system provided personalized recommendations based on similar users' viewing history.

### Conclusion:
The project successfully implemented a movie recommendation system using both item-based and user-based collaborative filtering techniques. The recommendation models were based on the similarity of movies or users’ rating behaviors. By combining user ratings, demographic data, and movie genres, this system effectively suggested relevant movies to users, improving the personalization of movie recommendations.
