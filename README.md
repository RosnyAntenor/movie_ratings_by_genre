# Movie Ratings by Genre

This project looks through movie ratings across various genres to understand how well different genres are received by critics and audiences.

# Key Findings
- Ratings tend to cluster around 60–70, with outliers in specific genres.
- Critics are more positive towards movies before the 1960s, while general audiences are more favorable towards movies after
- There has been a slow, but consistent downward trend towards the reception of movies sincethe 1930s to now, likely due to nuance and sample size

Visualization on Tableau: https://public.tableau.com/app/profile/rosny.antenor/viz/RottenTomatoesMovingRatings/Dashboard

<img width="1854" height="814" alt="Dashboard" src="https://github.com/user-attachments/assets/6c262d29-ad67-434b-8d9d-6977806fe181" />

# Data Source and Files
- Original Data: https://mavenanalytics.io/data-playground/movie-ratings
- 
- _Projects_Movie_Ratings.ipynb: Jupyter Notebook file using python to organize the data
- fixed_movie_rating_data.csv: Dataset exported after being cleaned on python

Below is a summarized version of my process throughout doing this project. For the full thing, which is messier, but shows it more truthfully, the file will be provided as "thought process.txt"

# Data Cleaning 

In Excel:

Realigning Data
- Ensured correct alignment of columns, addressing issues caused by misaligned or wrapped text.
- Filtered out rows lacking audience ratings to focus on meaningful comparisons.
- Standardized date formats to MM/DD/YYYY, correcting inconsistent entries and correcting erroneous years (2030s/2040s/2050s) using find-and-replace techniques

Choosing Columns

Removed irrelevant columns:

- movie_info
- consensus
- directors
- writers
- cast
- studio_name

Kept relevant columns:

- movie_title
- rating
- genre
- in_theaters_date
- on_streaming_date
- runtime_in_minutes
- tomatometer_status
- tomatometer_rating
- tomatometer_count
- audience_rating
- audience_count

In Python:

Null/Incorrect Data

- Dropped rows with null or missing movie_title
- Corrected runtime_in_minutes
- Filled missing genre entries

Parsing Genres

- Split multi-genre entries into separate rows for accurate genre-based analysis
- Determined a genre list of what would be used
- Added a year column extracted from release dates
- Corrected streaming release years using data validation

# Data Visualizations & Analysis

Still in Python: 
- Created simple visualizations using seaborn and matplotlib to explore potential rating trends.

Using Tableau
- Compared average ratings over time between critics and audiences.
- Made the findings and observations shown at the beginning of this README
- Analyzed ratings by genre, full visualization is at the top of this file
