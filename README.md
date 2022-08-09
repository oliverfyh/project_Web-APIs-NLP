# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP



## Goals
This project is to collect posts from two subreddits ('AskWomen' and 'AskMen') from www.reddit.com, and train two models (random forest and logistic regressin) to classify which subreddit a given post came from.

We will:
- collect posts Using Pushshift's API
- NLP with regex tokenizer, lemmatizer,  stemmer and tfidf-vectorizer
- train two models (random forest and logistic regressin) 
- 


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
- To use **ROC AUC** to compare model perforamce, because the **AUC metric** utilizes probabilities of class prediction. Based on that, we’re able to more precisely evaluate and compare the models.
    - The closer to 1, the better 'ROC AUC' is
    - perc_diff must be less than 5%
- To provide **Accuracy score** too. Since our data is balance and both positive and negative results are of same importance to us, **Accuracy score** is another good metric which is understandable and intuitive even to a non-technical person
    - The closer to 1, the better 'Accuracy' is
    - perc_diff must be less than 5%


## Results
- Two model have similar performance in term of ROC AUC score (around 0.85) and accuracy score (about 0.79). Logistic Regression model outperform slightly 
- 


## Future Enhancement
- The chosen Logistic Regression model has an accuracy score of 79%, which is not very promising. We may consider other models such SVM and AdaBoost.
- We may increase dataset size for better performance
    - We may fetch more posts, for example, from 2,000 to 4,000
    - We may fetch all related comments from each post

