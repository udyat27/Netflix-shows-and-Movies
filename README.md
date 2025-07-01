This project focuses on analyzing IMDb Movies and Shows data spanning the last 70 years. The dataset includes information such as ratings, number of votes, release year, and runtime for each title. The goal is to perform basic data cleaning and transformation, followed by visual exploration to uncover trends in ratings and runtimes, and to identify the top-rated movies and shows.
The dataset contains information on both Movies and Shows, with 5,283 records. It includes key details such as runtime, description, rating, votes, and release year. Below is a breakdown of the important columns:

**Id:** A unique identifier for each record. It helps in aggregating and analyzing trends, such as counting the number of titles released in a specific year.

**Release Year:** Covers a range from 1953 to 2022, roughly 70 years of data. However, some years (e.g., 1955, 1957) have missing entries.

**Title:** Includes the names of movies and shows—many of which are well-known—making the dataset engaging for exploration.

**Type:** Indicates whether a record is a "MOVIE" or a "SHOW". Useful for filtering and comparative analysis.

**Description:** While not essential for basic analysis, this field can be used for extracting keywords or performing genre classification using natural language processing techniques.

**Age Certification:** This field has a significant amount of missing data. As there's no reliable method to fill in the gaps, it will be retained as-is during analysis. Missing values may be handled case-by-case if needed.

**Runtime:** Indicates the duration of the movie or show in minutes. While not explicitly stated, it’s important to analyze the distribution, check for outliers, and understand the typical runtime range.

**IMDb_Score: **Represents the IMDb rating given by users, reflecting how well the movie or show was received by the audience.

**IMDb_Votes: **Shows the number of user votes on IMDb. Note that the reliability of the score may vary depending on the number of votes—titles with very few votes may have skewed or less reliable ratings.





The following data transformation and visualization tasks were completed as part of the analysis:

**Created a custom column** in Power Query Editor to calculate the overall impact score using the formula: Score × Votes.

**Added a new column runtime_hrs** using DAX by converting the runtime from minutes to hours.

**Implemented slicers for enhanced interactivity:
**
    runtime_hrs: Slicer style set to Between.
    
    release year: Slicer style set to Tiles.
    
    type: Slicer style set to Dropdown.

Visualized release trends:

    A donut chart showing the number of movies released per year.
    
    A pie chart showing the number of shows released per year.
    
    Both charts were filtered to include only movies/shows released after 2010.

Analyzed score-weighted engagement by visualizing how the average of rating × votes varies with runtime.

**Created a bar chart** showing how many movies were released in each age certification category since the year 2000.

**Combined analysis:**

    Plotted how score × votes varies across different age certifications.
    
    In the same visual, compared how average runtime (in hours) varies across certifications.

**Added data cards:**

    A title card to highlight the selected title.
    
    A multi-row card to display descriptions.
    
    Enhanced the final report with styling and formatting improvements for a cleaner and more intuitive user experience.


