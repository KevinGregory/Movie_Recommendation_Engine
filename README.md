# Movie_Recommendation_Engine

This repo contains files that I used to build out a movie recommendation engine, primary pulling from Kaggle's ml-25m movie dataset: https://www.kaggle.com/garymk/movielens-25m-dataset

I also used a few extra datasets that have been uploaded here. None of the datasets I could find linked movie ratings with movie reviews, so I built a web scraper to walk through the list of titles from IMDB and pull down all of the user reviews. This allowed me to conduct a tf-idf analysis on movie reviews, tie them to ratings and calculate cosine similarity scores based on a user's input.

Ultimately, there are two recommendation engines working here. The individual engine looks at the user's inputs and finds similarities to other movies based on genre, cast, crew, reviews etc. and weights the similarity based on the corresponding reviews. It then recommends the most similar movies to ones the user liked. The second engine maps the user to a cluster based on the ratings and recommends the top movies in that cluster. The clustering is conducted in the User Clustering file.
