# Movies-ETL

## Project Overview

This project will construct an automated pipeline that pulls in new data from Wikipedia, Kaggle metadata, and MovieLens rating data as part of the Amazing Prime Hackathon. It then applies the necessary transformations to the data before loading it into an existing PostgreSQL database. 
We utilised the following breakdown for this study:

1. write an ETL function to read three data files,
2. extract and transform the Wikipedia data,
3. extract and transform the Kaggle and rating data,
4. load the data to a PostgreSQL Movie Database.

## Resources

Kaggle data is used in the Movies-ETL. The MovieLens dataset of over 20 million reviews is used in the Kaggle dataset, which also includes a metadata file with information on the movies from The Movie Database (TMDb).

-   Data Source: wikipedia-movies.json, movies_metadata.csv, ratings.csv
-   Software: Python 3.7.9, Anaconda Navigator, Conda 4.8.4, Jupyter Notebook 6.3.0, PostgreSQL 11.11, pgAdmin 4

## Write an ETL function to read three data files

-   The function takes the Wikipedia JSON, the Kaggle metadata and MovieLens csv files and creates three separate DataFrames. 

## Extract and Transform the Wikipedia data

-   We filtered out the TV shows, consolidated the redundant data, removed the duplicates and formatted the Wikipedia data. 

## Extract and Transform the Kaggle and rating data

-   Again, we consolidated the redundant data, removed the duplicates, formatted and grouped the data.
-   The Kaggle and rating data were then merged with the Wikipedia movies DataFrame.

## Extract and Transform the Kaggle and rating data

-   The function in its final step connects to the database by sqlalchemy library and to_sql method.
-   Complete ETL process can be executed with a single function extract_transform_load call.

## Summary

The ETL programme gathered and cleaned movie data from various sources (Wikipedia JSON and Kaggle and ratings csv files). It integrates and modifies the data before loading it into two updatable PostgreSQL dataset tables for examination by the hackathon participants.
