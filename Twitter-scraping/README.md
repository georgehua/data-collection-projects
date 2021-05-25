## Twitter Scraping



**Tools Used:** BeautifulSoup, Selenium, chromedriver, Python (pandas)

**Repository**: https://github.com/georgehua/data-collection-projects/tree/main/Twitter-scraping

**Demo Notebook URL:** 

- Tweepy: https://georgehua.github.io/data-collection-projects/Tweepy.html
- Scweet: https://georgehua.github.io/data-collection-projects/Scweepy_example.html

**Availability Check:** 2021-04-30

**About the Project:** Each day Twitter generates a massive amount of data, and there's a lot of opportunities to analyze those tweets for different researches. But before doing all sorts of studies, the first step is always to collect data from Twitter. This repository evaluates different libraries or approaches to fetch data from Twitter. I also built demo programs to set up the pipeline from requesting data to parsing and save to ready-to-use CSV file.



### Approach 1: Official Twitter API Wrapper (Reliable, but has query limitation)

#### Tweepy 

Official Website: https://www.tweepy.org/

Tweepy is a Python library for accessing the Twitter API. It is great for simple automation and creating twitter bots. Tweepy has many features. Some main functionality it covers:

- Get tweets from our timeline.
- Creating and deleting Tweets.
- Follow and unfollow users.
- **Query tweets**

The maximum number of requests that are allowed is based on a time interval, some specified period or window of time. The most common request limit interval is 15 minutes. If an endpoint has a rate limit of 900 requests/15-minutes, then up to 900 requests over any 15-minute interval is allowed.



**Example Results:**

<img src="../docs/figures/twitter_results.png">



### Approach 2: Browser scripting tool (Unreliable, but no/few query limitation)



#### Scweet

Official Repository: https://github.com/Altimis/Scweet

Scweet scrap tweets between two given dates (start_date and max_date), for a given language and list of words or account name, and saves a csv file containing scraped data :

```
[UserScreenName, UserName, Timestamp, Text, Embedded_text, Emojis, Comments, Likes, Retweets, Image link, Tweet URL]
```

Scweet uses headless browser (selenium) to scrape data. Authentication is required in the case of followers/following scraping. It is recommended to log in with a new account (if the list of followers is very long, it is possible that your account will be banned).



**Example Results:**

| UserScreenName |     UserName |                Timestamp |                                              Text | Embedded_text | Emojis | Comments | Likes | Retweets |                                        Image link |                                       Tweet URL |
| -------------: | -----------: | -----------------------: | ------------------------------------------------: | ------------: | -----: | -------: | ----: | -------: | ------------------------------------------------: | ----------------------------------------------: |
|   sukhbir kaur | @sukhbxrkaur | 2020-04-01T04:19:03.000Z | Sunnybrook Hospital.\n#COVID19 #Coronavirusont... |               |        |        4 |    39 |       18 | [https://pbs.twimg.com/media/EUfacJbWAAIVi9A?f... | https://twitter.com/sukhbxrkaur/status/1245204. |



#### twitterscraper  (Not Available anymore)

Official Repository: https://github.com/taspinar/twitterscraper

A simple script to scrape Tweets using the Python package `requests`†to retrieve the content and `Beautifulsoup4` †to parse the retrieved content.

Twitter banned the tool at late 2020.