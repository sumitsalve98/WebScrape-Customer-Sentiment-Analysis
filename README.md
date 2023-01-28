# Product Sales & Customer Sentiment Analysis on Web-scraped Data

# Project Description

### 1. What was my motivation behind creating this project?

- To learn data science, you need to do data science and this is my approach from day 1.
- I found that learning new things while doing the project is more optimum than just learning random stuff from the internet that you never implement.
- This was my motive behind creating this project.
   
### 2. Why did I build this project?

- In the past few months I have created multiple projects while learning data analysis like web scraping, data cleaning, EDA, and market trends/text/Spatial analysis.
- These projects were created separately and they are not related to each other.
- I wanted to implement everything that I had learned from these mini-projects into one big project and build one end-to-end data analysis project.

### 3. What problems does this Analysis solve?

- Identifying trends & patterns in sales, Identifying top-selling/underperforming products.

- Identifying customer segments that are most important to a business, such as geographic locations.

- Customers complaint segmentation into sub categories by analyzing text of product reviews. eg:- Customer service issue, Refunds/Returns/Replacement issue, Delayed deliveries, Faults in product, Misleading price/advertising, Wrong product received, Unsafe products.

- Demographic and Time-Based Insights from positive and negative product reviews.



# Outline 

| SL. NO |      Outline      |
|:------:|:-----------------:|
|   1    | Executive Summary |
|   2    |   Introduction    |
|   3    |    Methodology    |
|   4    |      Results      |
|   5    |    Discussion     |
|   6    |    Conclusion     |
|   7    |     Appendix      |

# Executive Summary

### 1. Understanding customer needs and preferences: 

Sentiment analysis can be used to identify common themes and patterns in customer feedback, allowing businesses to better understand what customers want and need.
      
### 2. Identifying areas for improvement: 

By analyzing customer feedback, businesses can identify areas where they are falling short and need to make changes to improve customer satisfaction.
      
### 3. Monitoring of online reviews: 

Sentiment analysis can be used to monitor mentions of a brand or product on social media and online review sites, providing businesses with valuable insights into how they are perceived by the public.

### 4. Making data-driven decisions: 

Sentiment analysis can provide businesses with a large amount of data that can be used to make more informed and data-driven decisions.


# Introduction

The Sentiment analysis is used to determine the emotional tone behind a piece of text or it can be used to understand customer opinions and complaints toward a product or service. It is performed to gain insights into customer perceptions, identify areas for improvement, and track the effectiveness of customer service efforts. Additionally, it can be used to monitor social media and online reviews for mentions of a brand or product and can be used in a variety of industries including e-commerce, finance, and healthcare.

# Objectives

## Background

Analyzing the Webscraped Flipkart product reviews.

## Purpose

Identify the complaints of customers and find an area for improvement.

## Questions for Analysis

### Sales Questions:

1. What is distribution of price throughout the data?
2. Correlation between price and total sales
3. What price range has the most selling products?
4. What is the Distribution of price for each category of products?
5. What are the total sales by each product category?
6. What are the most popular brands and what do they sell?
7. What are the top 10 most-sold & least-sold products?
8. Which cities have more customers who are buying Luxury items?
9. What is the trend in sales by years?
10. What is the trend in sales by months?
11. What are the sales in each state of India?

### Sentiment Analysis Questions

1. What is the Distribution of avg ratings?
2. What are the most high-rated and most low-rated products by their 'avg rating'?
3. What are the most reviewed products?
4. What is the overall sentiment of the reviews?
5. What is the Category specific sentiment of the reviews?
6. Perform the Customer complaint segmentation by analyzing the text with specific keywords in it which are related to issues.
7. What is the percentage of different types of issues from negative revives of customers for each category of products?
8. Analyze the Total reviews, Total negative reviews, and Complaints inside the negatives for every product in a dataset.
9. Which product has more negative reviews in ratio to its total reviews?
10. Which Product is the most faulty according to customers?
11. Which product has a Customer service issue according to customers?
12. Which customer locations have the most delivery issues?
13. Plot the Folium heatmap of customer locations that have the most delivery issues.
14. Perform Time-Based Sentiment analysis on the most reviewed product of Flipkart

## Audience

Management, business leaders, or other individuals or groups within an organization who are responsible for making decisions based on the data.

# Hardware and Software Requirments

## Hardware

- intel core i7 
- 8gb ram

## Software

In case of local machine We are going to use the following softwares in this project :

Programming Language : [Python](https://www.python.org/)

IDE : [Jupyter Notebook](https://jupyter.org/)

Packages : [BeautifulSoop](https://pypi.org/project/beautifulsoup4/), [Pandas](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html), [Numpy](https://numpy.org/), [Matplotlib](https://matplotlib.org/), [Plotly](https://plotly.com/), [Folium](https://python-visualization.github.io/folium/).

API used : [geokeo](https://geokeo.com/)

# Methodology

## 1. Web Scraping customers reviews data.

### 1.1. The data was collected from: [Flipkart](https://www.flipkart.com/) by using python library [BeautifulSoop](https://pypi.org/project/beautifulsoup4/)

### 1.2. Arround 0.9 million product reviews were scraped for 7 categories as following:

|   categories    | reviews count |
|:---------------:|:-------------:|
|   smartphone    |    499742     |
| water purifier  |    104846     |
| washing machine |    102324     |
|   television    |     80370     |
|  refrigerator   |     63665     |
| air conditioner |     42454     |
|     laptop      |     24176     |


### 1.3. This raw data have following columns:

| prod_id | product_name | brand_name | category | price | sold | prod_url | customer_name | purchase_date | customers_city | rating | comment_head | comment |
|:-------:|:------------:|:----------:|:--------:|:-----:|:----:|:--------:|:-------------:|:-------------:|:--------------:|:------:|:------------:|:-------:|

- To see the code of Collecting this data by Web Scraping: [webscrape product reviews.ipynb](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/1.%20webscrape%20product%20reviews.ipynb)

- Download the Scraped Data Before cleaning: [raw_reviews.csv](https://drive.google.com/file/d/1_xqUoAi0tlfQmiMlQlK5q1hzKnEIg6LK/view?usp=sharing) 

## 2. Data Cleaning & Adding useful features

### 2.1. Removed rows where important values were missing.

### 2.2. Corrected data types

### 2.3. Corrected date format

### 2.4. Generated new features 'month', 'year' and 'short_name'

### 2.5. Identified outliers in prices of different products.

### 2.6. Saved dataframe into new csv: 

- To see the code of Cleaning the raw data: [Data Cleaning & adding useful features.ipynb](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/2.%20Data%20Cleaning%20%26%20adding%20useful%20features.ipynb)

- Download the Cleaned data: [processed_reviews.csv](https://drive.google.com/file/d/11_EYQah18pCO7LggEKwPObvCUURP69Gj/view?usp=sharing)


## 3. Web Scraping Latitude and Longitude coordinates for each customer location.

### 3.1. I have used the API provided by https://geokeo.com/ to scrape the coordinates and address of different locations in India.

### 3.2. From address i have extracted the state name and added it into the new feature 'state'

### 3.3. Scraped Latitude and Longitude of total 8986 unique customers locations from API.

### 3.4. This location data was merged with reviews data on key = 'customers_city' with left joint in pandas.

- To see the code of Scraping Latitude and Longitude: [scraping latitude and longitude with API.ipynb](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/3.%20scraping%20latitude%20and%20longitude%20of%20customer%20location%20with%20help%20of%20API.ipynb)

- Scraped latitude and longitude data: [coordinates_data.csv](https://drive.google.com/file/d/1pXjbQXRdj750Pq-7V_zKS8WUNfujohe2/view?usp=sharing)

- Reviews+coordinates data merged: [added_coordinates_reviews.csv](https://drive.google.com/file/d/1zhGF3NoS6FI2Wk7T6LK1omevtlUklZCH/view?usp=sharing)

- Indian states geojson file: [states_india.geojson](https://drive.google.com/file/d/1vaksJjEW89YXXsCIO4sWtercyq8IHtfY/view?usp=sharing)

## 4. Analysis of Sales

To see the code and step by step process of Data Analysis of Sales [EDA of Sales.ipynb](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/4.%20Basic%20EDA%20of%20Sales.ipynb)

- Updated data: [added_coordinates_reviews_2.csv](https://drive.google.com/file/d/1K6T8Oi9f0L50JkXj-xS8DXVgqAIDUWib/view?usp=sharing)

## 5. Customer Sentiment Analysis
 
To see the code and step by step process of Customer Sentiment Analysis: [customer sentiment analysis.ipynb](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/5.%20customer%20sentiment%20analysis.ipynb)

- Updated data: [added_coordinates_added_sentiments_reviews2.csv](https://drive.google.com/file/d/1SgaOCwIYC5TcSrYKrFBRw8XXdwljofkD/view?usp=sharing)

# Results

## Product Sales insights:

### 1. What is distribution of price throughout the data?

![Distribution of price violin.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20price%20violin.jpeg?raw=true)

![Distribution of price hist.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20price%20hist.jpeg?raw=true)

### Insights:

- mean, min, max price of products are 19667, 670, 250000 rupees respectively.

- Around 75% of products have price less than 50k 

### 2. Correlation between price and total sales

![Correlation between price and total sales.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Correlation%20between%20price%20and%20total%20sales.jpeg?raw=true)

### 3. What price range has the most selling products?

![Price range and Total sales.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Price%20range%20and%20Total%20sales.jpeg?raw=true)

![percentage of sales by price range.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/percentage%20of%20sales%20by%20price%20range.jpeg?raw=true)

### 4. What is the Distribution of price for each category of products?

![Distribution of price by category.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20price%20by%20category.jpeg?raw=true)

### 5. What are the total sales by each product category?

![Total sales by each product category pie.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Total%20sales%20by%20each%20product%20category%20pie.jpeg?raw=true)

![Total sales by each product category bar.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Total%20sales%20by%20each%20product%20category%20bar.jpeg?raw=true)

### 6. What are the most popular brands and what do they sell?

![Most popular brands.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Most%20popular%20brands.jpeg?raw=true)

![pivot table.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/pivot_table_showing_top_selling_brands_with_product_categories.png?raw=true)

### 7. What are the top 10 most-sold & least-sold products?

![Top 10 most sold products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2010%20most%20sold%20products.jpeg?raw=true)

![Top 10 least sold products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2010%20least%20sold%20products.jpeg?raw=true)

### 8. Which cities have more customers who are buying Luxury items?

![Cities with more customers who are buying Luxury items.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Cities%20with%20more%20customers%20who%20are%20buying%20Luxury%20items.jpeg?raw=true)

### 9. What is the trend in sales by years?

![The overall trend in sales by years.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/The%20overall%20trend%20in%20sales%20by%20years.jpeg?raw=true)

### 10. What is the trend in sales by months?

![Trend in sales by month.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Trend%20in%20sales%20by%20month.jpeg?raw=true)

### 11. What are the sales in each state of India?

![map.png](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/map.png?raw=true)

## Sentiment Analysis insights:

### 1. What is the Distribution of avg ratings?

![Distribution of avg ratings hist.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20avg%20ratings%20hist.jpeg?raw=true)

![Distribution of avg ratings violin.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20avg%20ratings%20violin.jpeg?raw=true)

![percentage distribution of ratings.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/percentage%20distribution%20of%20ratings.jpeg?raw=true)

### 2. What are the most high-rated and most low-rated products by their 'avg rating'?

![Top 10 highest rated products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2010%20highest%20rated%20products.jpeg?raw=true)

![Top 10 lowest rated products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2010%20lowest%20rated%20products.jpeg?raw=true)

### 3. What are the most reviewed products?

![Top 20 most reviewed products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2020%20most%20reviewed%20products.jpeg?raw=true)

### 4. What is the overall sentiment of the reviews?

![Polarity of sentiment.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Polarity%20of%20sentiment.jpeg?raw=true)

### 5. What is the Category specific sentiment of the reviews?

![Category specific Sentiment polarity.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Category%20specific%20Sentiment%20polarity.jpeg?raw=true)

### 6. Perform the Customer complaint segmentation by analyzing the text with specific keywords in it which are related to issues.

- Each negative customer review is scanned for a list of specific keywords that suggest potential issues the customer might have.

- These complaints are categorized into subcategories like Faulty products, Customer service, Refunds/Returns/Replacement, delivery, Misleading price/advertising, unsafe product, and Wrong product received.

![Distribution of types of complaints.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20types%20of%20complaints.jpeg?raw=true)

### 7. What is the percentage of different types of issues from negative revives of customers for each category of products?

![Product category specific complaints.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Product%20category%20specific%20complaints.jpeg?raw=true)

### 8. Analyze the Total reviews, Total negative reviews, and Complaints inside the negative review for every product in a dataset.

![Complaints inside the review.png](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Complaints%20inside%20the%20%20review.png?raw=true)

### 9. Which product has more negative reviews in ratio to its total reviews?

![Product with most negative reviews.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Product%20with%20most%20negative%20reviews.jpeg?raw=true)

- Word Cloud of most Badly reviewed product

Whirlpool 7.5 kg Fully Automatic Top Load with In-built Heater Grey

![Word Cloud of most Badly reviewed product.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/WordCloud%20of%20most%20Badly%20reviewed%20product.jpeg?raw=true)

### 10. Which Product is the most faulty according to customers?

![Most Faulty product.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Most%20Faulty%20product.jpeg?raw=true)

- WordCloud of most Faulty products reviews

Godrej 7 kg Fully Automatic Top Load with In-built Heater Grey

![WordCloud of most Faulty product by customer reviews.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/WordCloud%20of%20most%20Faulty%20product%20by%20customer%20reviews.jpeg?raw=true)

### 11. Which product has a Customer service issue according to customers?

![Product with most Customer service issues.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Product%20with%20most%20Customer%20service%20issues.jpeg?raw=true)

- WordCloud of product with Customer service issue

Whirlpool 7.5 kg Fully Automatic Top Load with In-built Heater Grey

![WordCloud of Products with most Customer service issues by customer](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/WordCloud%20of%20Products%20with%20most%20Customer%20service%20issues%20by%20customer%20reviews.jpeg?raw=true)

### 12. Which customer locations have the most delivery issues?

![locations with most delivery complaints.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/locations%20with%20most%20delivery%20complaints.jpeg?raw=true)

### 13. Plot the Folium heatmap of customer locations that have the most delivery issues.

![map_most-delivery-issues.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/map_most-delivery-issues.jpeg?raw=true)

### 14. Perform Time-Based Sentiment analysis on the most reviewed product of Flipkart

- REDMI 9i Sport (Coral Green, 64 GB) have most reviews count = 9500

![Polarity of reviews REDMI 9i Sport.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Polarity%20of%20reviews%20REDMI%209i%20Sport.jpeg?raw=true)

# Discussion

Technology Trends now and future

Training and Re-skilling workers

Females participation in Technology field

Bridge divide of technology gaps in developing countries

Eliminate age and education discrimination in employment

# Ovearall Findings and Implications

## Findings

1. Programming Languages- TypeScript is gaining significant interest and Python continues to grow as well.

2. Databases- Redis, Elasticsearch, PostgreSQL and MongoDB are gaining more interest.

3. Platforms- Interest Slack and Windows is dropping significantly.

4. WebFrames- Vue.js is gaining substantial interest and React.js continues to grow as well.

## Implications

1. Continue to staff enough JavaScript and HTML/CSS but employ more people skilled in TypeScript and Python.

2. Employ more people skilled in Redis, Elasticsearch, PostgreSQL and MongoDB.

3. Continue to staff enough ASP.NET but employ more people skilled in Vue.js and React.js.

4. Continue to staff enough Linux, employ more peopleskilled in Docker, AWS and Android, butmake reductionsto Slack and Windows.


# Conclusion

1. Carve out budget in order to hire additional staff with skills needed to fill any gaps.

2. Set aside budget or put a program in place to upskill those already employed.

3. Make adjustmentsin staff for those skills no longer in demand.

# Appendix

# Authors

- [@sumitsalve](https://github.com/sumitsalve98)


# 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://sumitsalve98.github.io/MyPortfolio/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sumit-salve-72b818217/)









