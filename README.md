<div id="top"></div>

<h1 align="center"> Reddit NLP Classification Analysis </h3>
  <img src='./images/pysql.png'> 

  <p align="center">
    Completed for General Assembly DSI Immersive
    <br />
  </p>
</div>



<!-- ABOUT THE PROJECT -->
# About The Project

### Executive summary
The goal of this analysis is to classify text posts as either belonging to one subreddit or another, using NLP.

Success will be evaluated using the model's accuracy score in correctly classifying the posts, with a second goal of trying many models to obtain the highest accuracy score possible.

### Subreddits
* r/learnpython is a subreddit for people who are learning python, mostly filled with resources and questions. r/learnsql is similar, except for people who are learning sql. 
* Both subreddits are fairly active, but r/learnpython is much more popular; it has 613k subscribers, compared to 17.7k subscribers for r/learnsql.

### Research Questions¶
* What preprocessing steps are best for creating a classification model with high accuracy?
* Which classification models and hyperparameters lead to the highest accuracy score?


### Dataset
For this project I used reddit's PushshiftAPI to pull rows of data. I was limited to making 60 requests per minute, and 100 rows of data per pull. 



## Data Cleaning & EDA
Data cleaning steps included dropping duplicate rows, filling NAs, and accounting for slightly unbalanced data. In MY EDA, I visualized distributions for average post length/word count as well as for number of comments; overall this exploratory analysis pointed to what we already knew, that r/learnpython is more active and has more subscribers than r/learnsql.


## Preprocessing
My preprocessing steps included train/test splitting, lemmatizing words, removing special characters, adding custom stopwords, and fitting both a countvectorizer and tfidfvectorizer (in order to see which one permed best). Overall, my countvecotorizer actually outperformed all models using tfidfvectorizer, even with hyperparams tuned.


## Modeling
I tried multiple different classfiers in this section but the top 3 performers were multinomialbayes, logistic regression, and a random forest. Tuning hyperparams with gridsearchcv/randomizedsearchcv did not improve scores by any significant, so I created an ensemble model with my three top performing models. 

This was the final model that I settled on, with an accuracy score on the test set of 92.4%, and a precision score of 93%.

## Conclusions:
* Due to computational limits I was not able to finish running XGBoost; this is something that I suggest someone should try if they're facing a similar classification problem.
* My final ensemble model outperforms all the single models, however the downside fo this is that's it's much more difficult to interpret compared to the others.
* Many of the misclassified posts had to do with topics that could fit easily in either subreddit, i.e. someone sharing generic learning resources, or questions about regex.
* Other frequent incidents included posts where selftext(body text) had been removed, and only a generic title remained... i.e. "I need help with a project." If more data was pulled and posts without body text were dropped from the dataframe, the model might perform better.


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/github_username/repo_name/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: images/screenshot.png

