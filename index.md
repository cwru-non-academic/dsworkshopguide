# Web Scraping

Web scraping is a technique used to collect information from the internet and save it so it can be analyzed as needed. Web scraping is usually done after a research question has been defined and will be part of the data gathering phase of the research lifecycle.

This course will walk you through using several different strategies and several different python libraries to scrape data from the web and analyze it.  We will learn:

- What web scraping is and why we would use web scraping to gather data
- About the HTTP request and reponse process that is the foundation of the web
- How to make requests and save the response from the web server(s)
- How to analyze the structure of web pages so we can scrape specific data
- How python scripts can be constructed to target specific data structures on web pages
- How to direct the web scraper to navigate through a series of pages and scrape each one

The content on the web is incredibly diverse, so web scraping scripts are usually custom built to target specific web sites and data.  These example projects will get you familiar with the various process and possibilities of web scraping so you can begin building a custom web scraper to target the web sites and information you are interested in.

### Digital Workshop Series
You can find the complete list of Digital Scholarhsip Workshops here: You can find a directory of the currently available tutorials here:  [https://librarybeales.github.io/dsworkshops/](https://librarybeales.github.io/dsworkshops/)

### Constellate or Binder?

Constellate is available to Case Western students, staff, and faculty.  To use Constellate you will have to create a JSTOR login that is separate from your University login.  Instructions for that are here:  <a href="https://librarybeales.github.io/CreateLogin/" target=blank>Making a Constellate Account</a>.

If you are not part of Case you can launch these tutorials using the Launch Binder button.  ![A binder launch button](https://mybinder.org/static/images/badge_logo.svg)  

Any changes you make or work you complete will be deleted when closing the tab or window.  You can, however, download a copy of file you've been working in before closing the browser.  

## Why scrape?  And when not to...

The content on the web is an unbelievably rich resource.  However, the information available can be difficult to collect and organize manually.  

For example, if you were interested in analyzing how people communicate on social media about the NASDAQ, you could manually search for posts tagged with #NASDAQ, copy and paste them or screen shot them, and then begin manually organizing the user names, likes, tags, text content, etc.  You would be limited in the sample size you could analyze by the amount of labor required.

If, however, you built a web scraper to crawl a site and capture every post with a #NASDAQ tag, you'd be able to capture a much larger sample size and save the data in an accessible format for future researchers.  Analysis of that data, also using python, would allow you to quickly see who posts the most, which posts have the most likes, what stock tickers are mentioned most frequestly in a given time span, etc.  

Additionally, the content on the web is constantly changing.  If you are basing your research on information from the web, it would be a good idea to store that infomation somewhere yourself, so that those who are evaluating your research can access the identical information.

In short, web scraping can make the endless data available online accessible, useful and permanent.

### Do I really need to web scrape?

Data is available from many sources across a wide variety of disciplines.  If you can find a relevant dataset, it will almost always be easier to use than something scraped from the web.  The data from web scraping usually need significant parsing and cleaning in order to be useful.  

So before you resort to web scraping, see if you can locate the data eleswhere. Contacting a research Librarian is an excellent first step.  Case Western also has a research data index here: <a href ="link!">Data Index</a> 


## Project #1: Making an HTTP Request and Receiving a Response

This first project will use the `requests` package to introduce the basic web scraping workflow.  All the lessons on this page use <a href="https://books.toscrape.com/">Books to Scrape</a> as the example website.  As you can probably tell from the name, this is a website set up specifically for practicing web scraping.

In this project you will:
1. Send a request to a web server.
2. Check for a response.
3. View the content of that response.
4. Write that content to a file. 

<a href="https://constellate.org/lab?repo=https%3A%2F%2Fgithub.com%2FLibraryBeales%2FWeb-Scraping&filepath=scrape1.ipynb" target="_blank">![A constellate launch button](https://constellate.org/images/constellate-badge.svg)</a>   <a href="https://mybinder.org/v2/gh/LibraryBeales/Web-Scraping/main?labpath=scrape1.ipynb" target="_blank">![A binder launch button](https://mybinder.org/static/images/badge_logo.svg)</a>


## Project #2: Exploring Website Structure and Getting Specific Data from Web Scraping 

Normally, in a web scraping project, you are looking for specific information.  You don't need to scrape the entire <a href="https://books.toscrape.com/">Books to Scrape</a> page if you are only interested in a list of book titles.  We are going to practice looking at the structure of a web page so we can design a web scraper that only retrieves certain infromation.  Once we understand the way the information we want is tagged and/or organized, we can create rules for the web scraper to follow.  The process of breaking down the parts of the web page to retrieve specific informaiton is frequently referred to as HTML parsing.

In this project you will:
1. Use the `Inspect` tool in your web browser to explore the structure of the <a href="https://books.toscrape.com/">Books to Scrape</a> website.
2. Understand how book titles on the site are tagged/classified. 
3. Understand and use a python script to crawl the web page and extract only the data that meets the classification criteria we identified for titles in step 2.
4. Look at the list of titles we scraped.  Identify problems with the data and explore an alternative strategy of using Beautiful Soup to get the correct titles.
5. Write the list of correct titles to a file. 

<a href="https://constellate.org/lab?repo=https%3A%2F%2Fgithub.com%2FLibraryBeales%2FWeb-Scraping&filepath=scrape2.ipynb" target="_blank">![A constellate launch button](https://constellate.org/images/constellate-badge.svg)</a>  <a href="https://mybinder.org/v2/gh/LibraryBeales/Web-Scraping/main?labpath=scrape2.ipynb" target="_blank">![A binder launch button](https://mybinder.org/static/images/badge_logo.svg)</a>


## Project #3: Scraping sets of related information into CSV files.

Build a scraper that collects multiple data points about each book based upon specific criteria.

In this project you will:
1. Determine what data we are able to collect about each book listed in the store.  
2. Use the `Inspect` tool in your web browser to identify the web page structure for those pieces of data. 
3. Understand and use a python script to crawl the web page and extract only the data that meets the classification criteria we identified in steps 1 and 2.
4. Write the data to a csv file. 

<a href="https://constellate.org/lab?repo=https%3A%2F%2Fgithub.com%2FLibraryBeales%2FWeb-Scraping&filepath=scrape3.ipynb" target="_blank">![A constellate launch button](https://constellate.org/images/constellate-badge.svg)</a>  <a href="https://mybinder.org/v2/gh/LibraryBeales/Web-Scraping/main?labpath=scrape3.ipynb" target="_blank">![A binder launch button](https://mybinder.org/static/images/badge_logo.svg)</a>

## Project #4: Scraping data from mulitple pages.

In this project you will:
1. Use the `Inspect` tool to explore how <a href="https://books.toscrape.com/">Books to Scrape</a> handles navigation between pages.
2. Understand and use a python script to direct the web scraper to a navigate to the next page if there is one, and scrape the specified data from there, and repeat this process until there are no more pages.
3. Examine the data to see if our scraper worked the way we think it should.
4. Write the data to a csv file. 

<a href="https://constellate.org/lab?repo=https%3A%2F%2Fgithub.com%2FLibraryBeales%2FWeb-Scraping&filepath=scrape4.ipynb" target="_blank">![A constellate launch button](https://constellate.org/images/constellate-badge.svg)</a>  <a href="https://mybinder.org/v2/gh/LibraryBeales/Web-Scraping/main?labpath=scrape4.ipynb" target="_blank">![A binder launch button](https://mybinder.org/static/images/badge_logo.svg)</a>

## Bonus Project: Data Visualization with Plotly.

In this project you will:
1. Examine the csv file we saved from the previous project and determine what values we would like to visualize.  
2. Look at the <a href="https://plotly.com/python/">Plotly</a> package for Python and determine which kinds of graphs we will could create with the data.  
3. Understand and use a python script to generate those graphs using the data we scraped from the <a href="https://books.toscrape.com/">Books to Scrape</a> website.
4. Save those graphs to a file.

[![Launch in Constellate badge](https://constellate.org/images/constellate-badge.svg)](https://constellate.org/lab?repo=https%3A%2F%2Fgithub.com%2FLibraryBeales%2FWeb-Scraping)  <a href="https://mybinder.org/v2/gh/LibraryBeales/Web-Scraping/main?labpath=scrape5.ipynb" target="_blank">![A binder launch button](https://mybinder.org/static/images/badge_logo.svg)</a>