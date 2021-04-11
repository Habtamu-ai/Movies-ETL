# Movies-ETL
## Overview
The main purpose of this project is to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. We refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data. Finally, we perform the ETL process by adding the data to a PostgreSQL database.
## Result

### ETL Function to Read Three Data
Using Python, Pandas, the ETL process, and code refactoring, we write a function that reads in the three data files and creates three separate DataFrames. Looking below three data frames screenshots.

![Wiki_movie_df](https://user-images.githubusercontent.com/78656720/114308083-9cc4d900-9ab0-11eb-8580-9824eb537c31.png)


![Kaggle_metadata_df](https://user-images.githubusercontent.com/78656720/114308092-a5b5aa80-9ab0-11eb-8fec-f16f8f5039d9.png)


![ratings_df](https://user-images.githubusercontent.com/78656720/114308095-a9e1c800-9ab0-11eb-8875-89d8ab069c6b.png)

### Extract and Transform the Wikipedia Data 
Using Python, Pandas, the ETL process, and code refactoring, we extract and transform the Wikipedia data so we can merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, we use a try-except block to catch errors.
![Wiki_movie_tolist](https://user-images.githubusercontent.com/78656720/114308435-fed20e00-9ab1-11eb-9c67-df1da6b38a3a.png)


### Extract and Transform the Kaggale metadata. 
Using Python, Pandas, the ETL process, and code refactoring, we extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Then, we merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, we merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.

### Create the Movie Database
Using Python, Pandas, the ETL process, code refactoring, and PostgreSQL we add the movies_df DataFrame and MovieLens rating CSV data to a SQL database.
Looking the table below we can seee we succefuly load our data in to our SQL database.
![movies_query](https://user-images.githubusercontent.com/78656720/114308868-4907bf00-9ab3-11eb-93ff-0950ffe01c24.png)
![ratings_query](https://user-images.githubusercontent.com/78656720/114308931-70f72280-9ab3-11eb-8dd7-efc68530e577.png)

## Summary
The main purpose of this project is to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. We refactor the code from this module and managed to create:
 1: An ETL function to read three data files
 2: Extract and Transform the Wikipedia Data
 3: Extract and Transform the Kaggle Data
 4: Create the Movie Database
