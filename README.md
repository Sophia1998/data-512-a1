# Data 512 A1: Data Curation Assignment

## Purpose of this project

  The goal of this assignment is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through September 30 2021. The whole process of implementation is fully documented and can be reproducible by others: from data collection to data analysis. At the end of the project, a time series visualization is produced, which shows Wikipedia traffic from various access sites: mobile app, mobile web and desktop. 

## Data Sources

  The data for this project are collected from the Wikimedia REST API, Wikimedia Foundation, 2018 https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions, which is is licensed under the CC-BY-SA 3.0 and GFDL licenses. 
CC-BY-SA 3.0: https://creativecommons.org/licenses/by-sa/3.0/
GFDL: https://www.gnu.org/licenses/fdl-1.3.html

Data for this project was gathered from two Wikimedia REST APIs:
1. Pagecounts API: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts
   
   Pagecounts API is a public API developed and maintained by the Wikimedia Foundation that serves analytical data about pagecounts of Wikipedia and its sister projects. Pagecount is the legacy definition of what we now call "Pageview". This API makes available the pagecounts aggregated per project from January 2008 to July 2016. 
3. Pageviews API: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews
   
   Pageviews API is a public API developed and maintained by the Wikimedia Foundation that serves analytical data about article pageviews of Wikipedia and its sister projects. With it, you can get pageview trends on specific articles or projects; filter by agent type or access method, and choose different time ranges and granularities; you can also get the most viewed articles of a certain project and timespan, and even check out the countries that visit a project the most.

## Final Data File Description 

(en-wikipedia_traffic_200712-202108.csv)
  
  year: From 2007 to 2021 (int)
  
  month: From 1 to 12 (int)
  
  pagecount_all_views: All page counts in month, year (int)
  
  pagecount_desktop_views: Desktop page counts in month, year (int)
  
  pagecount_mobile_views: Mobile page counts in month, year (int)
  
  pageview_all_views: All page views in month, year (int)
  
  pageview_desktop_views: Desktop page views in month, year (int)
  
  pageview_mobile_views: Mobile page views in month, year (int)
  
## Usage Considerations

One thing need to be noticed for anyone who use this data file:
The data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.
