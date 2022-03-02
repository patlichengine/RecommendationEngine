# Recommendations with IBM
## Introduction
For this project you will analyze the interactions that users have with articles on the IBM Watson Studio platform, and make recommendations to them about new articles you think they will like. Below you can see an example of what the dashboard could look like displaying articles on the IBM Watson Platform.

## In this project, I carried out the following tasks

## I. Exploratory Data Analysis
   I explored the data used int the project in order to draw some insights which I then used to answer key questions throughout the rest of the notebook.

## II. Rank Based Recommendations
   I started in building recommendations by looking at most popular articles simply based on the most interactions with users. Since there are no ratings for any of the articles, popularity of the articles was based on the interactions with users. Such articles were recommended to new users (or anyone depending on what we know about them). Here I provided two functions to get n top articles names and n top articles ids.

## III. User-User Based Collaborative Filtering
   In order to build better recommendations for the users of IBM's platform, ssers that are similar in terms of the items they have interacted with were considered. These items were then recommended to the similar users. Here specific insights were extracted as follows: 
   - Each user should only appear in each row once.
   - Each article should only show up in one column.
   - If a user has interacted with an article, then place a 1 where the user-row meets for that article-column irrespective of how 
     many times a user has interacted with the article.
   - If a user has not interacted with an item, then place a zero where the user-row meets for that article-column

## IV. Matrix Factorization
   Finally, I looked at a machine learning approach to building recommendations (Matrix Factorization). I usde matrix factorization to make article recommendations to the users on the IBM Watson Studio platform
