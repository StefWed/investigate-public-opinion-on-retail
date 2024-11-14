# Investigate Public Opinion about Retail Trade on Mastodon

#### -- Project Status: [Active]

## Project Intro/Objective
The purpose of this project is to investigate public opinion about different retailers (Migros - largest food retail in Switzerland; IKEA) - what do people share, what topics are on their minds when posting about these companies. For that purpose, posts from social media platforms are being scraped. The platform used is Mastodon, more precisely the Mastodon Social and the Mastodon World instances. By using this source of information, one can gain insights directly from customers around various things, like the reception of certain products, what products might be wished for, or of course image-related insights including sustainability, fairness, etc. It will give a variety of opinions, not only by those willing to fill in questionnaires for instance. These insights can be used by marketing, management or PR.

### Methods Used
* Web Scraping
* Cleaning a DataFrame using among others: the explode() function, the apply() function together with lambda function, defining functions for specific tasks together with lambda function
* Cleaning toots using Regex
* Explorative Data Analysis, word frequencies (with Natural Language Toolkit - nltk)
  
* to do: sentiment analysis

### Technologies
* Python
* Pandas, jupyter
* Requests, BeautifulSoup
* nltk
* itertools, collections

## Project Description
As pointed out before, posts from the Mastodon Social and Mastodon World instances are being scraped using the Mastodon API. 

The idea was to start with an in-depth example with lots of information around the set-up, the packages used and code explanations. So, the starting project is Migros on Mastodon Social. Using the Mastodon API and the requests function, posts with the hashtag #migros are scrapped for the last 2 1/2 years. For that timeframe not many posts were returned. The example shows how easy it is to store the result in a DataFrame. With help of the explode() function, the BeautifulSoup library (for the actual content which is in html) and some cases of apply() plus lambda function the Dataframe was cleaned.

In a next step, the hashtags were looked at. Which are most frequent, but also specific hashtags around the topic of sustainability plus the respectice content of the posts were extracted - to get an actual idea what people are posting around that topic. After that the general content of the toots was looked at closer, meaning word frequencies. To do so, the toots needed to be cleaned further. URLs were taken out, regex was useed to account for certain issues (like missing spaces between words), punctuation was removed, stopwords as well as collection words were removed to get a very clean list of toots, were counting makes sense. Obviously, the text needed to be splittedt in single words, the worde were put into lower case. After that itertools was used to flaten the list of lists (the list of toots) into one list of all the words. Finally collections was used to count and show the 25 most common words. Results can be found in the notebook, together with some interpretations.

(Followed by: IKEA on Mastodon)

## Getting Started

1. Clone this repo (for help see this [tutorial](https://help.github.com/articles/cloning-a-repository/)).
2. Create environment, install and load the libraries, modules, packages.
3. Open the Jupyter notebook Migros on Mastodon and go through it step by step.

   Lots of information, explanations as well as data cleaning included. This notebook can be seen as prototype and how-to example.
   Be prepared for spaghetti code ;). 
5. More advanced (without lots of info but with sentiment analysis): IKEA on Mastodon (work in progress)

## Featured Notebooks
* [Migros on Mastodon Prototype](https://github.com/StefWed/investigate-public-opinion-on-retail/blob/main/notebooks/Mastodon_Migros_Prototype.ipynb)
* [IKEA on Mastodon Prototype](https://github.com/StefWed/investigate-public-opinion-on-retail/blob/main/notebooks/Mastodon_Ikea_Prototype.ipynb)
