# [Crowdfunding](https://en.wikipedia.org/wiki/Crowdfunding)-scrape
Scraper for obtaining crowdfunding data in a structured manner on [fundrazr.com](https://fundrazr.com/) implemented in Python with Scrapy.

## Usage
To crawl the scraper, you need to install [Python 3](https://www.python.org/download/releases/3.0/), as well as the
[Scrapy](https://pypi.python.org/pypi/Scrapy) framework.

To install scrapy type the below command in the terminal:  
```
  pip3 install scrapy  
```  

To crawl the `main` spider for scraping pages, first navigate to the project folder then simply run the command

```
  scrapy crawl my_scraper
```

will scrape all information from [https://fundrazr.com/find?category=Health](https://fundrazr.com/find?category=Health).
By default, the scraped data will be stored (using Scrapy's [feed export](https://doc.scrapy.org/en/latest/topics/feed-exports.html))
in the `Data` directory as a (`.csv`) file following the naming convention:


    {Current UTC time}.csv

If you prefer a different output file name and format, you can specify this from the command line using Scrapy's `-o` option.
For example,

```
  scrapy crawl my_scraper -o Source1.csv
```

will output the data in CSV format as `Source1.csv`. (Scrapy automatically picks up the file format from the specified file 
extension).
