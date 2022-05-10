# class 17

## ****Web Scraping****

**Web scraping**, **web harvesting**, or **web data extraction** is data scraping used for extracting data from websites.

While web scraping can be done manually by a software user, the term typically refers to automated processes implemented using a bot or web crawler. It is a form of copying in which specific data is gathered and copied from the web, typically into a central local database
 or spreadsheet, for later retrieval or analysis.

### STEPS

Inspect the site to figure out where the links to the desired files are located.

Using the inspect option in the browser, inspect the data on the website

## **Python Code**

Import the following libraries.

```python
import requests
import urllib.request
import time
from bs4 import BeautifulSoup

```

set the url to the website and access the site with our requests library.

```python
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```

If the access was successful, you should see: < Response [200]>

Next we parse the html with [BeatifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) so that we can work with a nicer, nested BeautifulSoup data structure.

Use the method .findAll to locate all of the `<a>` tags

Extract the desired link

```python
one_a_tag = soup.findAll(‘a’)[38]
link = one_a_tag[‘href’]
```

notes taken from: [https://towardsdatascience.com](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)

## **Basic Rule: “Be Nice”**

An overarching rule to keep in mind for any kind of web scraping isBE GOOD AND FOLLOW A WEBSITE’S CRAWLING POLICIES

## **Respect Robots.txt**

Web spiders should ideally follow the robot.txt file for a website while scraping. It has specific rules for good behavior, such as how frequently you can scrape, which pages allow scraping, and which ones you can’t.

## **Make the crawling slower, do not slam the server, treat websites nicely**

Web scraping bots fetch data very fast, but it is easy for a site to detect your scraper, as humans cannot browse that fast. The faster you crawl, the worse it is for everyone. If a website gets too many requests than it can handle it might become unresponsive.
