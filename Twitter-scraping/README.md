# Tweets Querying Tools Evaluation
Each day Twitter generates a massive amount of data, and there's a lot of opportunities to analyze those tweets for different researches. But before doing all sorts of studies, the first step is always to collect data from Twitter. This repository evaluates different libraries or approaches to fetch data from Twitter. I also built demo programs to set up the pipeline from requesting data to parsing and save to ready-to-use CSV file.



### Approach 1: Official Twitter API Wrapper (Reliable, but has query limitation)

**Tweepy** (https://www.tweepy.org/) (Availability checked at 2021-04-30)

Tweepy is a Python library for accessing the Twitter API. It is great for simple automation and creating twitter bots. Tweepy has many features. Some main functionality it covers:

- Get tweets from our timeline.
- Creating and deleting Tweets.
- Follow and unfollow users.
- **Query tweets**

The maximum number of requests that are allowed is based on a time interval, some specified period or window of time. The most common request limit interval is 15 minutes. If an endpoint has a rate limit of 900 requests/15-minutes, then up to 900 requests over any 15-minute interval is allowed.



**Demo set up Link: https://georgehua.github.io/twitter-scrapper/Tweepy.html**



### Approach 2: Browser scripting tool (Unreliable, but no/few query limitation)

**Scweet** (https://github.com/Altimis/Scweet) (Availability checked at 2021-04-30)

Scweet scrap tweets between two given dates (start_date and max_date), for a given language and list of words or account name, and saves a csv file containing scraped data :

```
[UserScreenName, UserName, Timestamp, Text, Embedded_text, Emojis, Comments, Likes, Retweets, Image link, Tweet URL]
```

Scweet uses headless browser (selenium) to scrape data. Authentication is required in the case of followers/following scraping. It is recommended to log in with a new account (if the list of followers is very long, it is possible that your account will be banned).



**Demo set up Link: https://georgehua.github.io/twitter-scrapper/Scweepy_example.html**



**twitterscraper** (https://github.com/taspinar/twitterscraper) (Not Available anymore)

A simple script to scrape Tweets using the Python package `requests`†to retrieve the content and `Beautifulsoup4` †to parse the retrieved content.

Twitter banned the tool at late 2020.



