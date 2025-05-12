Task 1: Data Cleaning and Preprocessing
 Dataset Used:
Netflix Movies and TV Shows – A publicly available dataset from Kaggle containing metadata of movies and TV shows available on Netflix, including fields such as title, type, director, cast, country, release year, rating, and the date the content was added to Netflix.

 Objective:
The primary goal of this task was to clean and preprocess raw data to ensure it is accurate, consistent, and analysis-ready. This is a crucial step in any data analysis pipeline, as unclean data can lead to incorrect insights and flawed decision-making.

Cleaning and Preprocessing Steps:
Missing Values Handling:

Identified missing entries using .isnull().sum().

Filled missing values in critical categorical fields:

country, director, and cast columns were filled with 'Unknown' to retain the records without discarding valuable data.

rating column was filled with 'Not Rated' for consistency.

Removed records with missing values in essential columns such as title and type, as these are mandatory for identifying the content.

Date Format Standardization:

Converted the date_added column from object/string format to a standardized datetime format using pd.to_datetime().

This ensures consistency and allows for time-based analysis like release trends, seasonal content releases, etc.

Duplicate Removal:

Identified and removed duplicate rows using .drop_duplicates(), ensuring that no redundant records remain in the dataset.

Column Name Standardization:

Renamed all column headers to lowercase and replaced spaces with underscores for consistency and ease of use in Python (e.g., date_added instead of Date Added).

String Cleaning:

Stripped leading and trailing whitespaces from all string columns to ensure uniformity, especially helpful during grouping or filtering operations.

Data Type Checks:

Validated that all columns were of appropriate data types (datetime for dates, object for strings, etc.), ensuring compatibility with further analysis and visualization tools.

Final Output:
Cleaned dataset saved as netflix_titles_cleaned.csv

Python script for the cleaning process included.

README summarizing the entire task for documentation and evaluation.

Tools and Libraries Used:
Language: Python 3.x

Libraries:

pandas for data manipulation and cleaning

datetime support via pandas for handling date formats

 Deliverables:
Cleaned and well-structured CSV file

Python script or Jupyter Notebook used for processing

This README file for clear documentation

