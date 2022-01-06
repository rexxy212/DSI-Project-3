# Executive Summary
With the advent of social media, we are now more interconnected than ever
before. This connectivity comes at a price; misinformation is rampant on the
internet, and becomes a tool for fearmongering, economical, or even political
manipulation.

2000~ posts were scrapped from r/News, a legitimate news subreddit and r/TheOnion, 
a satirical news subreddit to determine if a model could be trained from the text in 
their titles to determine real or fake news. Data cleaning, exploratory data 
analysis were performed on the datasets to glean some insight
into which words more frequently appeared in their respective subreddits.

The datasets were then combined and Logistic Regression and Naive Bayes modeling
was performed to determine if there were any textual features that are
strong indicators of real or fake news. The Logistic Regression model fared
slightly better, with a relatively high ROC score of 0.914 and a Test score of
0.838.

Some words that were strong indicators of r/News were "US", "Covid" and "China",
whilst words that were strong indicators of r/TheOnion were "Trump", "Onion" and
"Nation".

# Problem Statement
The increasing popularity and reliance on social media as a source of
information worsens the problem of misinformation (fake news) today.

As a team of data scientist hired by a US government agency, we aim to analyse
and detect fake news using Natural Language Processing (NLP) using data from
r/News and r/TheOnion.

To analyse and detect fake news, Logistic Regression and Naive Bayes will be
performed on the title of posts. The test and ROC scores will be evaluated to
determine if the model is a success.

# Content
[1. Data Scrap & Preliminary Cleaning](https://git.generalassemb.ly/ken-tan/Project-3/blob/master/codes/1.%20Project%203%20Data%20Scrap%20%26%20Preliminary%20Cleaning.ipynb)

[2. Data Cleaning & Exploratory Data Analysis](https://git.generalassemb.ly/ken-tan/Project-3/blob/master/codes/2.%20Project%203%20Data%20Cleaning%20%26%20Exploratory%20Data%20Analysis%20.ipynb)

[3. Preprocessing and Modeling](https://git.generalassemb.ly/ken-tan/Project-3/blob/master/codes/3.%20Project%203%20Preprocessing%20and%20Modeling.ipynb)

# Findings
Top features for determining r/News are the words:
1. US
2. Covid19
3. China
4. Covid
5. killed

Top features for determining r/TheOnion are the words:
1. Trump
2. Onion
3. Nation
4. Coronavirus
5. Biden

# Conclusions
The relatively high ROC score of 0.914 and Test score of 0.838 attained
indicated that the model is quite successful in predicting whether a post was
real or satire based on the text in its headline.

Interestingly, the words Covid, Covid19, US and China were found to be better predictors of real news, whereas satire tends to use the term 
Coronavirus (instead of just Covid) and focused a lot more on the former and current US presidents, Trump and Biden. 
This could partly be due to wanting to include 'virus' in the naming for fearmongering purposes.

# Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**subreddit**|*object*|theonion_clean.csv|Which subreddit the post is from.|
|**title**|*object*|theonion_clean.csv|Title of post from Reddit.|
|**created_utc**|*float*|theonion_clean.csv|The time and date post was created in epoch.|
|**removed_by_category**|*object*|theonion.csv|Indicator of whether a post was deleted by its subreddit moderator.|
|**label**|*int*|theonion_clean.csv|Indicator to differentiate between r/TheOnion and r/News.|
|**date_posted**|*object*|theonion_clean.csv|The time and date post was created.|
|**length_text**|*int*|theonion_clean.csv|Length of the title of post.|

# Credits
r/News [Source](https://www.reddit.com/r/news/)

r/TheOnion [Source](https://www.reddit.com/r/TheOnion/)

Pushshift Reddit API [Source](https://github.com/pushshift/api)
