# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Classification of Reddit Posts

### Objectives

1. Collect posts from two subreddits using Reddit's API.
2. Use NLP to train a classifier on which subreddit a given post came from. This is a binary classification problem.


### Collecting Posts from Two Subreddits Using Reddit's API

The subreddits of choice were NBA and MLB. These are sports discussion threads on two different leagues, National Basketball Association and Major League Baseball. To acces the API, .json is added to the end of the url: https://www.reddit.com/r/mlb.json

Reddit gives 25 posts per request. To get enough data, Reddit's API was hit repeatedly in a for loop. time.sleep() function was added at the end of your loop to allow for a break in between requests.

---

### Data Cleaning and Extraction 

As many of the posts were images, the focus of this poject would be based on the thread titles. The titles were extracted with the subreddit it belonged to. The sample size of each subreddit (NBA:972 vs MLB:983) was checked to be similar in order to avoid a mismatch problem.

---

### Feature Extraction and Train-Test Split

Three feature selection methods were employed (**Count Vectorizer** and **TF-IDF**), to explore which method gave a better score for this classification problem. A 75-25 train-test split was defind to evaluate the accuracy of the model.

---

### Model Building and Testing

Two classification methods were selected for evaluation (**Multinomial Naive Bayes Classifier** and **Logistic Regression**). The metric for determining the best model coupled with the feature extraction method is the prediction accuracy of the test set.

---

### Best Performing Model

Logistic Regression yielded the best training scores (>97% accuracy) but the testing score was lower at around 91% accuracy. This might indicate overfitting of the training model resulting in high biasness. On the other hand, the difference between the training and testing accuracies for Multinomial Naive Bayes Classifier were smaller (around 4%). With this classifier, feature extraction by TF-IDF had a higher testing accuracy of 92%. This was identified as the best combination in this exercise. We study the confusion matrix of the best model below.

---