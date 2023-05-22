# Project 3: Subreddit Classification with Pushshift API and NLP
Analysis by Charles Ramey for General Assembly Data Science Immersive Course - Project 3

### Problem Statement

Hockey For Everyone ("HFE") is a fictional startup company whose mission is to design and sell affordable, high-quality hockey equipment that meets the needs of players of all backgrounds and abilities. This project aims to determine the most effective way to market hockey gear to reddit users by analyzing two subreddits: r/hockey and r/hockeyplayers. The goal is to identify which subreddit tends to focus more on non-professional hockey by analyzynig common words and phrases used in submissions to each subreddit. The project explores data scraped from Reddit using the Pushshift API, and tests a variety of classification machine learning models to accurately submissions by subreddit and provide the HFE marketing team with a tool to test advertisement language before rollout. 

---

### Summary

This project collected just under 200,000 total reddit submissions, including 149,940 and 49,987 from the r/hockey and r/hockeyplayers  subreddits, respectively.  After sufficiently cleaning the data, the datasets were reduced to approximately 63,000 total submissions, including 32,177 and 30,726 from r/hockey and r/hockeyplayers, respectively. The title and body text of all submissions were investigated for language trends and verbiage that distinguishes one subreddit from the other. In particular, the two subreddits were evaluated for language indicative of a user demographic that may be receptive to the advertisement of affordable, high-quality hockey equipment. Exploration of the text revealed that r/hockey is more geared towards discussion of professional hockey, whereas r/hockeyplayers exhibited terminology and phrasing consistent with hockey players seeking hockey-related advice.

In the second phase of this project, seven different classification machine learning models were trained and tested on their ability to accurately classify reddit submissions by the correct subreddit, r/hockey or r/hockeyplayers. Logistic regression and adaptive boosting methods proved most successful, however all models were stacked and a logistic regression model was trained on the predictions of all seven models in order to optimize the model's performance. The final model achieved a classification accuracy of 95% on both training and testing datasets, giving HFE enough confidence to use the model as a tool to test marketing language


---

### Conclusion and Recommendations

The conclusion of this project is that the subreddit r/hockeyplayers would be best suited to support HFE's first Reddit marketing campaign. This subreddit primarily hosts content focused on non-professional hockey, where user submissions are typically seeking hockey recommendations and advice. Hockey equipment is a common discussion subject within r/hockeyplayers, making it an exceptional place to advertise HFE's low-cost, high-quality gear. While r/hockey is a larger forum for hockey discussions in general, the content focuses primarily on professional hockey, with little content regarding the equipment of non-professional hockey players. HFE can gain confidence in the language of its reddit marketing posts by testing them using the final model developed herein and know that the advertisement is targeting the correct audience.

The subreddit r/hockeyplayers is a great place for HFE to begin its equipment marketing campaign on Reddit, however there are additional avenues for expansion and improvement if the initial strategy proves successful:
- r/hockeygoalies: Goalies play a key role on every hockey team, yet they have some of the most expensive equipment which makes the position out of reach for many new hockey players. This subreddit could help HFE reach a demographic with a high demand for affordable hockey gear.
- Youth hockey: Hockey is inaccessible for many young athletes due to the cost of equipment and the constant need to size up equipment as a child outgrows their current gear.
- Alternative forums and social platforms: Reddit has a wide user base, but HFE can expand by applying the lessons learned from this project to future projects that investigate platforms such as Facebook, Twitter, or other hockey-centric forums.

---

### Sources

1. [https://www.reddit.com/r/hockey/](https://www.reddit.com/r/hockey/)
2. [https://www.reddit.com/r/hockeyplayers/](https://www.reddit.com/r/hockeyplayers/)
3. [https://www.ibm.com/topics/natural-language-processing](https://www.ibm.com/topics/natural-language-processing)
4. [https://medium.com/mcd-unison/using-pushshift-api-for-data-analysis-on-reddit-b08d339c48b8](https://medium.com/mcd-unison/using-pushshift-api-for-data-analysis-on-reddit-b08d339c48b8)
5. [http://api.pushshift.io/redoc#operation/search_reddit_subreddits_reddit_search_subreddit_get](http://api.pushshift.io/redoc#operation/search_reddit_subreddits_reddit_search_subreddit_get)
6. [https://www.epochconverter.com/](https://www.epochconverter.com/)
7. [https://stackoverflow.com/questions/47423854/sklearn-adding-lemmatizer-to-countvectorizer](https://stackoverflow.com/questions/47423854/sklearn-adding-lemmatizer-to-countvectorizer)
8. [https://pandas.pydata.org/docs/reference/index.html](https://pandas.pydata.org/docs/reference/index.html)
9. [https://scikit-learn.org/stable/modules/classes.html](https://scikit-learn.org/stable/modules/classes.html)
10. [https://matplotlib.org/stable/api/index.html](https://matplotlib.org/stable/api/index.html)
11. [https://stackoverflow.com/questions](https://stackoverflow.com/questions)
12. [https://xgboost.readthedocs.io/en/stable/python/python_api.html](https://xgboost.readthedocs.io/en/stable/python/python_api.html)