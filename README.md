# FLIPKART-GRID-4.0
EXTRACT TRENDS FROM SOCIAL MEDIA

## INTRODUCTION
This system was developed by Devanshi Bavaria and Dhruv Shah as part of Flipkart Grid 2022. The aim of this system is to help fashion retailers in identifying trend-setting and best selling products on Flipkart webiste.

## DESIGN
This system is broken down into 3 important parts:

### SCRAPERS
<li>Used to scrape data from various social media. Currently sites which are scraped include trending tweets from twitter.</li>
<li>All this raw scraped data is currently stored on Drive, with links to it being stored on an Atlas database.</li>
<li>These scrapers are designed to run automatically after a fixed amount of time, so that fresh trending data is always being scraped.</li>
<li>Implemented using libraries like selenium, tweepy etc in python.</li>

### MODELS
