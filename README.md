# Reddit-Post-Classifier

# Contents
 - [Summary](#Summary) 
 - [Problem Statement](#problem-statement) 
 - [Project Steps](#project-steps) 



## Summary
The final model evaluated in this project provides the best subreddit category to post in amongst two chosen, so that users can know the best related subreddit.


## Problem Statement
You might want to send a post, or asking a question on Reddit, but you are stuck with two subreddit to post it to, but don’t know which subreddit you should choose to ask your question in. The idea in this project is suggesting Reddit company to add a new feature where before posting your question or any kind of post you choose two subreddits you think are most relevant to your post, and let the engine decide which one of these two subreddit your post belongs to. Using NLP and Machine learning models on two subreddit posts, given a new post, model could predict which of these subreddit the post belongs to, and then you can send your post in that subreddit.

## Project Steps
- Data acquisition: Data was collected from Reddit using Reddit's API. We are building a binary predictor using NLP, and machine learning to determine which subreddit category is more suitable to post our post in. 

- Data processing: First a function is developed to pull posts from Reddit, a data frame of around 20000 records is collected from each chosen subreddits, and after applying preprocessing steps we have left with almost 80% to 90% of data. Then data were merged and a class of either of categories were assigned to each data frame. Two categories chosen for this project are “Gaming” and “Music”, but any other categories can be chosen very simply by replacing their name in the function for requesting posts through API. 
To show our keyword metadata (most common words) before preprocessing which helps
to visualize importance of preprocessing. Since we are looking for words frequency and we want to develop machine learning models, we must prepare the text and convert it to a more digestible form for machine learning algorithms. Text is Preprocessed including (Removal of links, numbers, emojis, stop words) then Stemming and Tokenizing is used which are re some of the most fundamental natural language processing tasks.
Then I did feature extraction including Instantiated and fitted CountVectorizer and TF-IDF Vectorizer to already preprocessed text to get the words frequencies and to map from textual data to real valued vectors to feed in machine learning models.

- Model training: Using the data processed as described above, the text classifier model is fed training data that consists of feature vectors for each text, different machine learning models were developed and used to predict the class a text sample is more related to including Naive Bayes Classifier, Logistic Regression and Random Forest Model. The best result is for Naive Bayes with count vectorizer with 92% accuracy for testing dataset and 98% accuracy for training dataset.

