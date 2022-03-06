# Recommendations with IBM
## Introduction
This project made use of data from IBM Watson Studio platform to build recommendation engines about new articles one think they will like. Below you can see an example of what the dashboard could look like displaying articles on the IBM Watson Platform.

## In this project, I carried out the following tasks

## I. Exploratory Data Analysis
   The data exploration stage of the project was meant to look at the structure of the data and estimate descriptive statistics of the data. I also used a histogram to show the pictoral represention of the data. The descriptive analysis also enabled me to answer specific questions about the data like:
   - The number of unique articles that have an interaction with a user.
   - The number of unique articles in the dataset (whether they have any interactions or not).
   - The number of unique users in the dataset. (excluding null values)
   - The number of user-article interactions in the dataset.

## II. Rank Based Recommendations
   This recommendation process focues on the popularity of an article which used the number of times each user has interacted on an article to make recommendations for other neighboring users. Here I completed the functions for:
   - getting top articles from a DataFrame for a specific number of query per time
   - getting associated article ids used to estimate other articles that could be recommended to a user

## III. User-User Based Collaborative Filtering
   In order to build better recommendations for the users of IBM's platform, users that are similar in terms of the items they have interacted with were considered. I reshaped the data frame to convert the articles column to a column headers while assigning where anteraction occured to a 1 and 0 otherwise  These items were then recommended to the similar users. Here specific insights were extracted as follows: 
   - Each user should only appear in each row once.
   - Each article should only show up in one column.
   - If a user has interacted with an article, then place a 1 where the user-row meets for that article-column irrespective of how 
     many times a user has interacted with the article.
   - If a user has not interacted with an item, then place a zero where the user-row meets for that article-column

## IV. Matrix Factorization
   Finally, I looked at a machine learning approach to building recommendations (Matrix Factorization). I usde matrix factorization to make article recommendations to the users on the IBM Watson Studio platform
