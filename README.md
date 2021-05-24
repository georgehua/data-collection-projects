# Data Collection Projects


Collection of data collection projects with web scraping and API tools. Including Twitter, LinkedIn



## LinkedIn Job Posting Scraping 

**Tools Used:** BeautifulSoup, Selenium, chromedriver, Python (pandas)

**Availability Check:** 2021-05-24

**About the Project:**

When I was looking for jobs on the LinkedIn job board, I found the built-in sorting system didn't provide enough functionalities to help me choose the most suitable jobs to apply to. And I was thinking to extract job descriptions from the LinkedIn platform and built my personal job boards. The first thing I need to start is collecting data from LinkedIn.

So, I went to the LinkedIn API documentation, but didn't find any luck from there, since the provided API endpoints are very limited. So, I decided to scrape the data with BeautifulSoup and Selenium. This notebook is the demonstration of setting up an extraction pipeline for searching `data analyst` position in `Greater Toronto Area, Canada`. I fetched the data using a headless browser to simulate human browsing behavior, then formatted and saved the data into a pandas data frame, eventually exporting it to a CSV file.

After running the pipeline, we will get the following information about the job posting:

- Date
- Title
- Company Name
- Location
- Job Description
- Job Level
- Job Type
- Function
- Industry
- Job ID



**Example Saved Results:**

| Job ID     | Date       | Company Name | Post                  | Location                     | Description                                                  | Level               | Type                     | Function                           | Industry                                                     |
| ---------- | ---------- | ------------ | --------------------- | ---------------------------- | ------------------------------------------------------------ | ------------------- | ------------------------ | ---------------------------------- | ------------------------------------------------------------ |
| 2553709029 | 2021-05-17 | Tucows       | Data Analyst - Remote | Toronto, Ontario, Canada     | Tucows (NASDAQ:TCX, TSX:TC) is on a mission to make the Internet better by providing people everywhere with online access to be empowered to make individual contributions... | Entry level         | Full-time                | Information Technology             | Information Technology and Services, Computer Software, and Internet |
| 2552463476 | 2021-05-24 | VetSuccess   | Business Analyst      | Toronto, Ontario, Canada     | The Role Working closely with project stakeholders, the Business Analyst will define the business requirements and functional specifications... | Entry level         | Full-time                | Information Technology and Analyst | Veterinary and Information Technology and Services           |
| 2542029589 | 2021-05-10 | ContentFly   | Data Analyst          | Toronto, Ontario, Canada     | ContentFly (YC W21) is one of the fastest growing B2B startups in the world. Building the Mailchimp for Content Marketing, we've grown to nearly $4m ARR in a year with a small team, no sales or dedicated marketing. We just closed a $10m Series A with Tier 1 funds like Khosla Ventures & YCombinator... | Mid-Senior level    | Full-time                | Analyst                            | Marketing and Advertising, Computer Software, and Internet   |
| 2547021172 | 2021-05-20 | Yelp         | Data Analyst          | Mississauga, Ontario, Canada | Must-Have • Analytical and problem-solving skills • Interpreting data, analyzing results using statistical techniques • Statistical methods to analyze data and generate useful business reports • Good communication skills • Positive attitude... | Good-to-Have Skills | • Data Mining experience | • Data Mining experience           | Information Technology and Services                          |