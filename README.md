# Movie Recommender Project Readme

This movie recommender project is a simple content-based recommendation system that suggests movies similar to a user-specified movie. It leverages natural language processing techniques to analyze movie features like genres, keywords, taglines, cast, and directors to find similarity scores between movies and provide recommendations based on those scores.

## Project Overview

The project can be broken down into the following main steps:

1. **Data Loading**: The movie data is loaded from a CSV file named 'movies.csv' using the Pandas library.

2. **Data Preprocessing**: Missing values in selected features (genres, keywords, tagline, cast, and director) are filled with empty strings.

3. **Feature Engineering**: A new feature named 'combined_features' is created by concatenating selected movie features, separated by spaces.

4. **Text Vectorization**: The TfidfVectorizer from Scikit-Learn is used to convert the 'combined_features' into a TF-IDF (Term Frequency-Inverse Document Frequency) matrix, which quantifies the importance of words in the combined features.

5. **Cosine Similarity**: Cosine similarity scores are calculated between the TF-IDF vectors of all movies. These scores represent the similarity between each pair of movies.

6. **User Input and Movie Matching**: The user provides a movie title, and a close match to the input title is found using the `difflib.get_close_matches` function.

7. **Recommendation Generation**: The most similar movies to the user's selected movie are determined by sorting the similarity scores. The top 30 recommended movies are then displayed.

## Example

For instance, if the user input is 'Iron Man,' the system finds 'Iron Man' as a close match and suggests the following movies:

1. Iron Man
2. Iron Man 2
3. Iron Man 3
4. Avengers: Age of Ultron
5. The Avengers
6. Captain America: Civil War
7. Captain America: The Winter Soldier
8. Ant-Man
9. X-Men
10. Made

## Setup and Usage

1. Ensure you have the required libraries (NumPy, Pandas, Scikit-Learn) installed.
2. Place your movie dataset (in this example, 'movies.csv') in the project directory.
3. Run the Python script provided in your preferred development environment.
