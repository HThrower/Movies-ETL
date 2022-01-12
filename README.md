# Movies-ETL
This project was an introduction tp performing an Extract, Transform, Load (ETL). The data set Movie data originates from Wikipedia, Kaggle and  implement a rating systsem on order to create a movie database from a clean dataset. The cleaning set incorporates cleaning rows and formating datatypes, preforming joins, and loading the cleaned dataset into a SQL database.

# Overview
Our intention is to create an automated pipline that can ETL proccess we previously did manually. A synopsisv of the movie dataset comes from 1990 to 2018 and combining the information from 3 different resources.

# Results
## ETL_function_test.ipynb
- Data is extracted from the website in JSON and CSV formats.
-Data is transformed into Pandas data frames.
-JSON file requires extra step – loading file first and then transforming into data frame.
![image](https://user-images.githubusercontent.com/31675832/149044887-9f52aadf-bb60-4fb2-90d0-8fbebc3026f8.png)
![image](https://user-images.githubusercontent.com/31675832/149044970-4b785742-a516-4ffa-96cb-d258133b7f5b.png)

## ETL_clean_wiki_movies.ipynb
- Function clean_movie combines scattered data of alternative languages into one column alt_titles.
- Its subfunction change_column_name organizes column names into consistent pattern.
- In the function extract_transform_load the transformation process of wiki movies data begins and includes:
  * Python list comprehensions.
  * apply() and map() methods in combination with lambda functions.
  * regular expressions or RegEx.
 ![image](https://user-images.githubusercontent.com/31675832/149045070-cebeba72-628b-4e44-9c86-ba526e4a9f65.png)
![image](https://user-images.githubusercontent.com/31675832/149045077-bedf381c-46f0-44c4-a770-983379011139.png)

 
 ## ETL_clean_kaggle_data.ipynb
 - Function extract_transform_load gets new tasks for cleaning Kaggle data and includes:
  * Changing datatypes, using methods pd.to_numeric, astype() and python comparison operators for Boolean types.
  * Filling missing values and filtering unwanted columns.
  *  Merging data frames using pd_merge method.
![image](https://user-images.githubusercontent.com/31675832/149044743-ce0cfce7-5401-43b1-99dc-e10fa3f9580c.png)
![image](https://user-images.githubusercontent.com/31675832/149044767-a9b14a8e-0a5c-4549-ab41-5f2262a725a7.png)


## ETL_create_database.ipynb
- The function in its final step connects to the database by sqlalchemy library and to_sql method.
- Complete ETL process can be executed with a single function extract_transform_load call.

The final results created a movies table with 6,052 rows. We see a reduction by 17% from the original of 7,311 and a ratings table with 26,024,289 rows.


# Resources
- Software: Python 3.7.9, Anaconda 4.9.2, Jupyter Notebooks 6.1.4, PostgreSQL 4.28
- Libraries: Pandas, SQLAlchemy, NumPy
- Files: Wikipedia Json, Movie Database Metadata, and MovieLens Ratings
-
