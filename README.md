# Investigate Public Opinion about Retail Trade on Mastodon

#### -- Project Status: [Active]

## Project Intro/Objective
The purpose of this project is to investigate public opinion about different retailers (Migros - largest food retail in Switzerland; IKEA) - what do people share, what topics are on their minds when posting about these companies. For that purpose, posts from social media platforms are being scraped. The platform used is Mastodon, more precisely the Mastodon Social and the Mastodon World instances. By using this source of information, one can gain insights directly from customers around various things, like the reception of certain products, what products might be wished for, or of course image-related insights including sustainability, fairness, etc. It will give a variety of opinions, not only by those willing to fill in questionnaires for instance. These insights can be used by marketing, management or PR.

### Methods Used
* Web Scraping
* Cleaning a DataFrame using among others: the explode() function, the apply() function together with lambda function, defining functions for specific tasks together with lambda function
* Cleaning toots using Regex
* Explorative Data Analysis, word frequencies (with Natural Language Toolkit - nltk)
* Sentiment Analysis
* Data Visualization

### Technologies
* Python
* Pandas, Jupyter, Regex
* Matplotlib
* Requests, BeautifulSoup
* nltk
* itertools, collections
* TextBlob

## Project Description
The project uses the Mastodon API to scrape posts from the Mastodon Social and Mastodon World instances. The first example focuses on posts containing the hashtag #migros, starting from January 1, 2022. While relatively few posts were found, they were largely informative, with minimal customer feedback about products or preferences. The example highlights how to store results in a DataFrame and clean the data using libraries such as BeautifulSoup (for HTML content) and Python's apply() with lambda functions. The explode() function was used to handle lists in DataFrame columns.

Hashtag analysis followed, identifying frequently used hashtags and those related to sustainability. The respective content of the posts was extracted to understand discussion themes. To analyze word frequencies, further text cleaning was performed, including removing URLs, fixing formatting issues with regex, and eliminating punctuation, stopwords, and collection words. After splitting the text into lowercase words, itertools flattened the list, and collections identified the 25 most common words. Bigram analysis was conducted to uncover relationships and themes, confirming the overall informative nature of the posts.

A second notebook focused on #ikea, with posts scraped from the Mastodon World instance. Here, functions were introduced to streamline tasks like scraping and cleaning. Python's input() function made the process interactive, allowing users to specify hashtags and date ranges. Results were stored in a CSV file to avoid repeated API calls and potential blocks. This sub-project also included sentiment analysis using the TextBlob library. The concepts of polarity and subjectivity were explored, with results visualized in plots. Limitations of TextBlob in analyzing short, informal Mastodon posts were discussed, suggesting the need for alternative tools for better sentiment accuracy.

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
