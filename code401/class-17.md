# Web Scraping




Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort. This is a great exercise for web scraping beginners who are looking to understand how to web scrape.

> Important notes about web scraping, Read through the website’s Terms and Conditions to understand how you can legally use the data. Make sure you are not downloading data at too rapid a rate because this may break the website.


- The first thing we need to do is find out where to find the links to the files we want to download, within several levels of HTML tags. Simply put, there is a lot of code on the website and we want to find relevant pieces of code that contain our data. 

Python Code

We start by importing the following libraries.

```python 
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```

Next, we set the url to the website and access the site with our requests library.

```python 
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```

Next we parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure. If you are interested in learning more about this library


```python 
soup = BeautifulSoup(response.text, “html.parser”)
```

We use the method .findAll to locate all of our ```<a>``` tags.


```python 
soup.findAll('a')
```

steps [here](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)

---------------

## What is Web Scraping?

Web scraping, web harvesting, or web data extraction is data scraping used for extracting data from websites. The web scraping software may directly access the World Wide Web using the Hypertext Transfer Protocol or a web browser. While web scraping can be done manually by a software user, the term typically refers to automated processes implemented using a bot or web crawler.

## How to scrape websites without getting blocked

It has specific rules for good behavior, such as how frequently you can scrape, which pages allow scraping, and which ones you can’t. Some websites allow Google to scrape their websites, by not allowing any other websites to scrape. This goes against the open nature of the Internet and may not seem fair, but the owners of the website are within their rights to resort to such behavior. Txt file on websites.

- User-agent: *

What if you need some data that is forbidden by Robots. Most anti-scraping tools block web scraping when you are scraping pages that are not allowed by Robots. By looking for a few indicators that real users do and bots don’t. Humans are random, bots are not. Humans are not predictable, bots are.

- Scraping too fast and too many pages, faster than a human ever can

No human ever does that.

- Too many requests from the same IP address in a very short time

You can do this by specifying a ‘User-Agent’.


Web scraping bots fetch data very fast, but it is easy for a site to detect your scraper, as humans cannot browse that fast. If a website gets too many requests than it can handle it might become unresponsive. Ideally, put a delay of 10-20 seconds between clicks and not put much load on the website, treating the website nice. Use auto throttling mechanisms which will automatically throttle the crawling speed based on the load on both the spider and the website that you are crawling.

- Do not follow the same crawling pattern

Web scraping bots tend to have the same crawling pattern because they are programmed that way unless specified. Sites that have intelligent anti-crawling mechanisms can easily detect spiders by finding patterns in their actions and can lead to web scraping getting blocked.

- Make requests through Proxies and rotate them as needed

When scraping, your IP address can be seen. When we send requests from a proxy machine, the target website will not know where the original IP is from, making the detection harder. Create a pool of IPs that you can use and use random ones for each request.

- Free Proxies

They are cheaper than residential proxies and could be detected easily. Residential Proxies, if you are making a huge number of requests to websites that block to actively. These are very expensive . Try everything else before getting a residential proxy.

