# Movies-ETL

## Background

Amazing Prime Video is platform for streaming movies and TV shows on Amazing Prime, the world’s largest online retailer. The Amazing Prime Video team wanted to create an algorithm to predict which low budget movies being released would become popular so they can buy the streaming rights at a bargain. We helped one employee, Britta gather data from both Wikipedia and Kaggle, combine them, and save them into a SQL database so that hackathon participants have a clean dataset to use. To do this, we followed the ETL process: extract the Wikipedia and Kaggle data from their respective files, transform the datasets by cleaning them up and joining them together, and load the cleaned dataset into a SQL database.

After completing the dataset, we were tasked with one final assignment-- to help Amazing Prime keep the database updated on a daily basis. Specifically, we are working to help Britta create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. 


## Overview

We were tasked with the following tasks:

- Deliverable 1: Write an ETL Function to Read Three Data Files
- Deliverable 2: Extract and Transform the Wikipedia Data
- Deliverable 3: Extract and Transform the Kaggle data
- Deliverable 4: Create the Movie Database

## Resources
- Software: Python, Jupyter Notebook, PostgresSQL
- Data Sources: wikipedia.movies.json, movies_metadata.csv, ratings.csv 


## Results

### Deliverable 1: Write an ETL Function to Read Three Data Files
- For the first deliverable, we successfully wrote a function that reads in the three data files and creates three separate DataFrames. See [ETL_function_test.ipynb](https://github.com/MichaelaAnastasiaAustin/Movies-ETL/blob/main/ETL_function_test.ipynb) file for the three data frames.


### Deliverable 2: Extract and Transform the Wikipedia Data
- For the second deliverable, we converted the cleaned Wikipedia data into a Pandas DataFrame-- the DataFrame is displayed in the following file: [ETL_clean_wiki_movies.ipynb](https://github.com/MichaelaAnastasiaAustin/Movies-ETL/blob/main/ETL_clean_wiki_movies.ipynb).


### Deliverable 3: Extract and Transform the Kaggle data
- For the third deliverable, we extracted and transformed the Kaggle metadata and MovieLens rating data, then converted the transformed data into separate DataFrames. Then, we merged the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame, and merged the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df. (See [ETL_clean_kaggle_data.ipynb](https://github.com/MichaelaAnastasiaAustin/Movies-ETL/blob/main/ETL_clean_kaggle_data.ipynb).


### Deliverable 4: Create the Movie Database
- Finally, in deliverable four, we added the movies_df DataFrame and MovieLens rating CSV data to a SQL database. See images of queries below.

Movies query
![movies](https://github.com/MichaelaAnastasiaAustin/Movies-ETL/blob/main/Resources/movies_query.png)

Ratings query
![ratings](https://github.com/MichaelaAnastasiaAustin/Movies-ETL/blob/main/Resources/ratings_query.png)



## Summary

All in all, we successfully created one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.

