## Data:
The dataset contains details of movies, including:

Movie title (original_title)
Genres (genres)
Cast
Director
Keywords (keywords)
Ratings (vote_average)

## Methodology:

Data Preprocessing:

Extracting relevant data fields.
Converting genres, cast, and keywords data from string format to lists.
Encoding categorical data like genres, director, cast, and keywords to binary format. Each genre, cast member, director, or keyword is given a unique binary representation in the dataset.
Similarity Measurement:

Using the Similarity function, the cosine distance is computed for genres, cast, director, and keywords between two movies. The distances are then summed up to get an overall similarity score.
Getting Nearest Neighbors:

The getNeighbors function is used to fetch the K most similar movies to a given movie. This is done by computing the similarity of the given movie with every other movie in the dataset, sorting them by similarity, and selecting the top K.
Rating Prediction and Recommendation:

The predict_score function is used to:
Fetch the K most similar movies to the provided movie title.
Recommend these movies to the user along with their genres and ratings.
Predict the rating of the provided movie by averaging the ratings of its K neighbors.
Display the predicted rating along with the actual rating of the provided movie.

## Outcome:
When the user provides a movie title, the system:

Recommends K movies that are similar to the given movie.
Predicts a rating for the given movie based on the ratings of its similar movies.
Shows the actual rating of the movie for comparison.