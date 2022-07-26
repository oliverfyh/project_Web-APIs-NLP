# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP



## Goals
This project is to collect posts from two subreddits ('AskWomen' and 'AskMen') from www.reddit.com, and train two models (random forest and logistic regressin) to classify which subreddit a given post came from.

We will:
- collect posts Using Pushshift's API
- NLP with regex tokenizer, lemmatizer,  stemmer and tfidf-vectorizer
- train two models (random forest and logistic regressin) 
- analyse contribution of top 20 important features


## Dataset and Data Directory

- One dataset is collected from https://www.reddit.com/r/AskWomen/, which contains 2000 posts with 70 columns 

- The other dataset is collected from https://www.reddit.com/r/Askmen/, which contains 2000 posts with 70 columns 

- Some important features are listed as below 


|Feature|Type|Description|
|---|---|---|
|**subreddit**|*String*|subsidiary threads or categories within the Reddit website. | 
|**author**|*String*|The author of a post fetched from the subreddit|
|**title**|*String*|The title of a post fetched from the subreddit|
|**selftext**|*String*|The body text of a post fetched from the subreddit|




## Metrics
- To use `ROC AUC` to compare model performance
    - The closer to 1, the better `ROC AUC` is
    - perc_diff must be less than 5%
- To provide `Accuracy score` too. Since our data is balance and both positive and negative results are of same importance to us, `accuracy score` is another good metric which is understandable and intuitive even to a non-technical person
    - The closer to 1, the better 'Accuracy' is
    - perc_diff must be less than 5%


## Results
- We built random forest model and logistic regression model. Logistic regression model outperformed in term of ROC AUC and Accuracy Score. 
- feature importance analysis show 65% of top important features are favorable to 'AskWomen'
- stopwords play an important role in this model, mostly because abbreviations of stopwords such as 'whn','hw' occurs much more frequently in "AskMen". 


## Future Enhancement
- The chosen Logistic Regression model has an accuracy score of 79%, which is not very promising. We may consider other models such SVM and AdaBoost.
- We may increase dataset size for better performance
    - We may fetch more posts, for example, from 2,000 to 4,000
    - We may fetch all related comments from each post

