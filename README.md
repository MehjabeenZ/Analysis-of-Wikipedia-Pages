# Homework 1: Professionalism & Reproducibility

This repository contains the data files, code and results of Homework 1, for the course Data 512: Human Centered Data Science at the University of Washington's MS in Data Science program. 

## Goal of Assignment

The goal of this assignment is to construct, analyze, and publish a dataset of monthly article traffic for a select set of pages from English Wikipedia from July 1, 2015 through September 30, 2023. 

## Resources Used
- Editor used: VS Code
- Python version: 3.9.12
- Packages used: json, time, requests, urllib, pandas, seaborn, matplotlib, tqdm

## API Documentation
- [Pageviews API documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)
- [Pageviews API endpoint](https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)
- [Wikimedia Foundation REST API terms of use](https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions)


## Project Organization

This project has the following structure:

```
.
├── data/
│   ├──academy_monthly_cumulative_201507-202309.json
│   ├── academy_monthly_desktop_201507-202309.json
│   ├── academy_monthly_mobile_201507-202309.json
│   └── thank_the_academy.AUG.2023.csv
├── results/
│   ├── Max_Min_Average_plot.png
│   ├── Top_10_Peak_Page_Views_plot.png
│   └── Fewest_months_plot.png
├── code/
│   ├── Monthly Article Traffic Analysis.ipynb
├── LICENSE
└── README.md
```
## Data 

Source Files:
- [Movies List](https://docs.google.com/spreadsheets/d/1A1h_7KAo7KXaVxdScJmIVPTvjb3IuY9oZhNV4ZHxrxw/edit?usp=sharing)
- [Sample API Notebook](https://drive.google.com/file/d/1XjFhd3eXx704tcdfQ4Q1OQn0LWKCRNJm/view?usp=sharing). This code is provided under the [Creative Commons](https://creativecommons.org) [CC-BY license](https://creativecommons.org/licenses/by/4.0/). Revision 1.2 - August 14, 2023

Intermediary Files:

- academy_monthly_mobile_start201507-end202309.json: Monthly mobile page traffic. 
- academy_monthly_desktop_start201507-end202309.json: Monthly desktop page traffic.
- academy_monthly_cumulative_start_201507-end202309.json: Monthly cumulative data is the sum of all mobile, and all desktop traffic per article.

Each JSON file is organised as an array of arrays. The larger array represents a single movie and the nested array within each larger array holds JSON objects that represent the pageviews for a particular month for that movie. The following is a description of each of the fields present in the JSON objects:

|Key name|Data Type|Description|
|---|---|---|
|`project`|`string`|the name of the project|
|`article`|`string`|the article(s) you want to retrieve data for|
|`granularity`|`string`|the granularity of data to return; "daily" or "monthly"|
|`timestamp`|`string`|The timestamp of the returned datapoint|
|`agent`|`string`|The type of agent that is considered when returning the number of views|
|`views`|`int`|The number of page views for the article at a timestamp that falls within the range for the given agent type|

## Results

### 1. Maximum Average and Minimum Average

### 2. Top 10 Peak Page Views

### 3. Fewest Months of Data

## Special Considerations
- The API call takes a considerable amount of time. To account for lag, a try/except block of code has been added. 


