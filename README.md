# Web-Scrapper
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1MjFmXBeGeZW9dPR9jY7-lnjK53btoGTs#scrollTo=6VL1-eCm9--O)


# Web-Scrapper
In this Project I scraped amazon URLs using bs4 to Scarpe the following details from the page.
1. Product Title
2. Product Image URL
3. Price of the Product
4. Product Details

The URL are in format of "https://www.amazon.{country}/dp/{asin}".
The country code and Asin parameters are in the Xlsx file in the repository
The CSV file contains 1000 rows. 
If any URL throws Error 404 then the {URL} is not available is printed  and the url is skipped.
After completing each round of hundred URLs the total time it 
took to complete them is also mentioned in the output file.
The output is in the list of dictionaries, finally represented in JSON(output.json file).

#how the web scrapper works


First to bypass the Amazon captcha we use rotating proxies with random user agent
To rotate user agents in Python 

1. Collect a list of User-Agent strings of some recent real browsers.
2. Put them in a Python List.
3. Make each request pick a random string from this list and send the request with the ‘User-Agent’ header as this string.

A rotating proxy is a proxy server that allocates a new IP address from a set of proxies stored in the proxy pool.
For Rotating Proxies :
 scrapy-rotating-proxies
 This package provides a Scrapy middleware to use rotating proxies, check that they are alive and adjust crawling speed.

A output JSON file is created and output after every iteration is saved in the json file.
An output json file is given in the repository.

Time for execution of program for 100 order of computations is calculated and entered in the directory.
Finally the directory is updated in the Json output file.
