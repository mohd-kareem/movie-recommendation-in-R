# movie-recommendation-in-R

Movie Recommendation System
This project implements a movie recommendation system using R, leveraging collaborative filtering techniques to suggest movies to users based on their ratings. The system uses the recommenderlab, ggplot2, and data.table libraries for data manipulation and visualization.

Prerequisites
To run this project, you will need:

R (version 3.5 or higher)
RStudio (optional, but recommended)
Required R packages:
recommenderlab
ggplot2
data.table
reshape2
You can install the required packages using:

R
Copy code
install.packages(c("recommenderlab", "ggplot2", "data.table", "reshape2"))
Dataset
The project uses two datasets:

movies.csv: Contains movie metadata (IDs, titles, genres).
ratings.csv: Contains user ratings for the movies (user IDs, movie IDs, ratings).
Make sure these CSV files are in your working directory or update the paths accordingly.

Data Overview
The movies.csv dataset includes the following columns:

movieId: Unique identifier for each movie.
title: Title of the movie.
genres: Genre(s) of the movie.
The ratings.csv dataset includes:

userId: Unique identifier for each user.
movieId: Unique identifier for each movie (matching movies.csv).
rating: Rating given by the user to the movie.
Data Preprocessing
The script includes steps for:

Data Loading: Load the movie and rating data using read.csv().
Genre Processing: Split genres and create a binary genre matrix.
Rating Matrix Creation: Convert the ratings data into a format suitable for collaborative filtering.
Data Normalization: Normalize ratings to ensure consistency.
Recommendation Model
The recommendation system uses Item-Based Collaborative Filtering (IBCF) to suggest movies to users:

Similarity Calculation: Compute user-user and item-item similarities using the cosine method.
Model Training: Train the recommendation model on a subset of the data.
Prediction: Generate movie recommendations based on the trained model.
Visualization
Several visualizations are included to help understand the data:

Bar plots for the total views of the top films.
Heatmaps for user and movie similarities.
Distribution plots for average ratings per user.
Running the Project
To run the project, follow these steps:

Set Working Directory: Ensure your working directory contains the movies.csv and ratings.csv files.

R
Copy code
setwd("path/to/your/directory")
Source the Script: Copy and paste the entire R script into your R console or save it as an .R file and run it.

Explore Recommendations: After running the script, check the recommendations for different users by modifying the predicted_recommendations output.

Example Output
The recommendations for the first user will be displayed as a list of movie titles.
Visualizations will be generated to provide insights into the data and model performance.
Conclusion
This movie recommendation system demonstrates the use of collaborative filtering techniques to provide personalized movie suggestions. You can further enhance the model by experimenting with different parameters and algorithms available in the recommenderlab package.

License
This project is open-source. Feel free to modify and distribute as needed.
