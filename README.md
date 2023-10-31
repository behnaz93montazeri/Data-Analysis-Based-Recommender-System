# Data Analysis-Based Recommender System

## Overview
This project presents a data analysis-based recommender system that provides movie recommendations based on user preferences and correlations between movies. It addresses the challenge of ensuring relevant recommendations by taking into account the number of ratings for each movie.

## Methodology
This recommender system follows these key steps:

1. **Data Merging**: Two datasets, one containing user informations (such as user id and ratings) and the other movie details (movie tile and item id), are merged to create a comprehensive movie database.

2. **Data Exploration**: A new data frame is created, containing movie titles, average ratings, and the number of ratings. Data visualizations are used to examine the relationship between the number of ratings and movie ratings. The observation is that, as the number of ratings increases, the movie ratings tend to rise.
   
![download](https://github.com/behnaz93montazeri/Data-Analysis-Based-Recommender-System/assets/124638983/49161865-92e0-44f0-b4ab-58fd4a61187f)

4. **Pivot Table Creation**: A pivot table is constructed with movies in columns and users in rows. The ratings are placed as values in the pivot table.

5. **Movie Selection and Correlation**: Three random movies are selected, and separate data frames are created for each movie, containing all users' ratings. The correlation between these movies and the main pivot data frame is calculated. NaN values are dropped to clean the data.

6. **Filtering Correlations**: A challenge arises with movies that have very few ratings, resulting in high correlations with the selected movie. To address this, the number of ratings is joined to the correlation tables. We then filtered movies with more than 100 ratings and sorted them in descending order of correlation. The top recommended movies are the ones with the highest correlations.

## Limitations
This data analysis-based recommender system has some limitations:
- It relies solely on correlations and does not consider cost functions, which are common in collaborative filtering systems.
- When movies have very few ratings, the system may recommend irrelevant movies. To mitigate this, the system selects movies with more than 100 ratings. This is a common issue with the Collaborative Filtering recommneder systems as well.
- Normalization can also help address the issue of sparsity and the impact of less-rated or unrated movies in a Collaborative Filtering (CF) recommender system.

## Usage
To run the Python script contained within this project's Jupyter notebook, follow these steps:
**Jupyter Notebook Environment**: Ensure that you have a Jupyter Notebook environment set up on your local machine, along with a Python distribution that supports the required libraries.
**Data Preparation**:
- Ensure that both datasets, "Movie_Id_Titles" and "u.data", are located in the same directory as the Jupyter notebook.




