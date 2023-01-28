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

#### - Removed rows where important values were missing.

#### - Corrected data types

#### - Corrected date format

#### - Generated new features 'month', 'year' and 'short_name'

#### - Identified outliers in prices of different products.

#### - Saved dataframe into new csv: 

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

### Insights:

- Products with price range of 10k to 30k are the most sold on flipkart.

### 3. What price range has the most selling products?

![Price range and Total sales.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Price%20range%20and%20Total%20sales.jpeg?raw=true)

![percentage of sales by price range.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/percentage%20of%20sales%20by%20price%20range.jpeg?raw=true)

### Insights:

- Price range 0-25000 rupees have most selling products. 681743 products are sold within this price range. That covers up to 74.3% of total sales.

- 195547 products are sold in price range of 25000-50000. That covers up to 21.3% of total sales.

- Sales decreased drastically for products with prices of more than 100000 rupees

### 4. What is the Distribution of price for each category of products?

![Distribution of price by category.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20price%20by%20category.jpeg?raw=true)

### Insights:

- Among all the other product categories laptops have the most varying price range and the most expensive product in our data set is also a laptop with a price of 250k.

### 5. What are the total sales by each product category?

![Total sales by each product category pie.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Total%20sales%20by%20each%20product%20category%20pie.jpeg?raw=true)

![Total sales by each product category bar.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Total%20sales%20by%20each%20product%20category%20bar.jpeg?raw=true)

### Insights:

- Smartphone is most selling product category on flipkart. Its total sales are 499742 which covers up to 54.5% of total sales.

- The laptop is the least sold category on Flipkart. Its total sales are 24176 which cover 2.63% of total sales

- Water purifier, Washing machine, television have similar numbers of sales.

### 6. What are the most popular brands and what do they sell?

![Most popular brands.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Most%20popular%20brands.jpeg?raw=true)

![pivot table.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/pivot_table_showing_top_selling_brands_with_product_categories.png?raw=true)

### Insights:

- Samsung, realme and poco are top three most popular while motorola, vivo and kent are least popular brands.

- Samsung also have more product categories than others like:- air conditioner, refrigerator, smartphones, television and washing machine.

### 7. What are the top 10 most-sold & least-sold products?

![Top 10 most sold products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2010%20most%20sold%20products.jpeg?raw=true)

![Top 10 least sold products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2010%20least%20sold%20products.jpeg?raw=true)

### Insights:

- Samsung Galaxy F22 and redmi 9i Sport are the top selling products on flipkart with sales around 10k.

- HP victus with ryzen 5 hexa core 5600H and Asus with ryzen 9 octa core 10nth gen are the least sold products on flipkart with sales of only 1 qnt.

### 8. Which cities have more customers who are buying Luxury items?

![Cities with more customers who are buying Luxury items.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Cities%20with%20more%20customers%20who%20are%20buying%20Luxury%20items.jpeg?raw=true)

### Insights:

Cities, where most of the expensive items are being sold, are

- Bengaluru
- Hyderabad
- New Delhi
- Chennai
- Pune
- Mumbai

### 9. What is the trend in sales by years?

![The overall trend in sales by years.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/The%20overall%20trend%20in%20sales%20by%20years.jpeg?raw=true)

### Insights:

- Since we only have data of products which are launched in a recent year we cannot find a proper trend in sales for older products or products which are probably dead now.

### 10. What is the trend in sales by months?

![Trend in sales by month.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Trend%20in%20sales%20by%20month.jpeg?raw=true)

### Insights:

October, November, and December are months when sales are the highest

### 11. What are the sales in each state of India?

![map.png](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/map.png?raw=true)

### Insights:

- UP, Maharashtra and West Bengal are the states with highest sales of 68884 to 103325 products.

## Sentiment Analysis insights:

### 1. What is the Distribution of avg ratings?

![Distribution of avg ratings hist.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20avg%20ratings%20hist.jpeg?raw=true)

![Distribution of avg ratings violin.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20avg%20ratings%20violin.jpeg?raw=true)

![percentage distribution of ratings.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/percentage%20distribution%20of%20ratings.jpeg?raw=true)

### Insights:

- Average Rating is 4.26 star
- 61.8% products have 5 star
- 7.77% products have 1 star

### 2. What are the most high-rated and most low-rated products by their 'avg rating'?

![Top 10 highest rated products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2010%20highest%20rated%20products.jpeg?raw=true)

![Top 10 lowest rated products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2010%20lowest%20rated%20products.jpeg?raw=true)

### 3. What are the most reviewed products?

![Top 20 most reviewed products.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Top%2020%20most%20reviewed%20products.jpeg?raw=true)

### 4. What is the overall sentiment of the reviews?

![Polarity of sentiment.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Polarity%20of%20sentiment.jpeg?raw=true)

### Insights:
- We have around 696706 reviews that have positive feedback and 182602 reviews with negative feedback.

### 5. What is the Category specific sentiment of the reviews?

![Category specific Sentiment polarity.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Category%20specific%20Sentiment%20polarity.jpeg?raw=true)

### Insights:

- Refrigerators have the most positive reviews. It has only 16% of negative reviews 

- Air conditioner have 25% of negative reviews.

### 6. Perform the Customer complaint segmentation by analyzing the text with specific keywords in it which are related to issues.

- Each negative customer review is scanned for a list of specific keywords that suggest potential issues the customer might have.

- These complaints are categorized into subcategories like Faulty products, Customer service, Refunds/Returns/Replacement, delivery, Misleading price/advertising, unsafe product, and Wrong product received.

![Distribution of type of complaints.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Distribution%20of%20type%20of%20complaints.jpeg?raw=true)

### Insights:

In the total negative reviews, we have 
- 28.6% complaints about Faults in product
- 8.93% complaints about Customer service issues
- 8.13% complaints about Refund/Return/Replacement
- 4.11% complaints about delivery issues
- 3.61% complaints about Misleading price/Advertisements
- 0.22% unsafe product & 0.016% Wrong product received type of complaints

### 7. What is the percentage of different types of issues from negative revives of customers for each category of products?

![Product category specific complaints.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Product%20category%20specific%20complaints.jpeg?raw=true)

### Insights:

- Television has the most (35.7%) complaints about Product defects/faults.
- Air Conditioner has the most (18.2%) complaints about customer service-related problems.
- Refrigerators have the most (9.88%) and (7.15%) complaints about refund/return/replacements and delivery.

### 8. Analyze the Total reviews, Total negative reviews, and Complaints inside the negative review for every product in a dataset.

![Complaints inside the review.png](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Complaints%20inside%20the%20%20review.png?raw=true)

### 9. Which product has more negative reviews in ratio to its total reviews?

![Product with most negative reviews.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Product%20with%20most%20negative%20reviews.jpeg?raw=true)

#### Word Cloud of most Badly reviewed product

![Word Cloud of most Badly reviewed product.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/WordCloud%20of%20most%20Badly%20reviewed%20product.jpeg?raw=true)

### Insights:

- product name - Whirlpool 7.5 kg Fully Automatic Top Load with In-built Heater Grey is most badly reviewed product.
- Positive words: Good, price, delivery, features, spin time, automatic stains.
- Negative words: inlet pipe, water inlet, performance, daily use, purchase, two stars.

### 10. Which Product is the most faulty according to customers?

![Most Faulty product.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Most%20Faulty%20product.jpeg?raw=true)

#### WordCloud of most Faulty products reviews

![WordCloud of most Faulty product by customer reviews.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/WordCloud%20of%20most%20Faulty%20product%20by%20customer%20reviews.jpeg?raw=true)

### Insights:

- Product name- Godrej 7 kg Fully Automatic Top Load with In-built Heater Grey is having more products faults.
- Positive words: Thanks flipkart, washing performance, fabulous working, service, installation man, good aesthetics, delivery
- Negative words: washer, bad quality, body.

### 11. Which product has a Customer service issue according to customers?

![Product with most Customer service issues.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Product%20with%20most%20Customer%20service%20issues.jpeg?raw=true)

#### WordCloud of product with Customer service issue

![WordCloud of Products with most Customer service issues by customer](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/WordCloud%20of%20Products%20with%20most%20Customer%20service%20issues%20by%20customer%20reviews.jpeg?raw=true)

### Insights:

Product name- Whirlpool 7.5 kg Fully Automatic Top Load with In-built Heater Grey is having more complaints about customer service.

### 12. Which customer locations have the most delivery issues?

![locations with most delivery complaints.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/locations%20with%20most%20delivery%20complaints.jpeg?raw=true)

### Insights:

- Orai, Uttar Pradesh and Pune, Maharashtra are two locations that are having most delivery-related issues

### 13. Plot the Folium heatmap of customer locations that have the most delivery issues.

![map_most-delivery-issues.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/map_most-delivery-issues.jpeg?raw=true)

### Insights:

- Locations that are near the border of China, Nepal, Bhutan, and Bangladesh are having delayed delivery.

### 14. Perform Time-Based Sentiment analysis on the most reviewed product of Flipkart

- REDMI 9i Sport (Coral Green, 64 GB) have most reviews count = 9500

![Polarity of reviews REDMI 9i Sport.jpeg](https://github.com/sumitsalve98/WebScrape-Customer-Sentiment-Analysis/blob/master/images/Polarity%20of%20reviews%20REDMI%209i%20Sport.jpeg?raw=true)

### Insights:

- It's clear that this product is improving with time.
- In the same timeline it is having much more positive feedback compared to negative.
- positive reviews are increasing at a very high rate while negative reviews are increasing at a much slower rate

# Discussion

### Limitations of this study:
- This dataset was scraped from the reviews section of Flipkart for each product, and it has only the information that was available on the webpage. 
- Flipkart doesn't allow us to scrape all data like the exact number of sales.
- Flipkart also doesn't like 1 stars reviews and they silently delete some of them.
### Suggestions for future research:
- Building an NLP model for sentiment analysis can help a business understand how customers feel about their products or services.
- This information can be used to improve customer satisfaction and make strategic decisions about product development and marketing. 
- An NLP model for sentiment analysis can provide valuable insights that can help a business be more successful.

# Conclusion

1. The average rating is 4.26 stars and around 82.6% of total ratings fall under 4 and 5. It means most customers are satisfied with the service.
2. We have around 696706 reviews that are predicted as positive feedback and 182602 reviews that are predicted as negative feedback. Again the number of positive feedback is very high compared to negative ones.
4. Television is the category with the most positive reviews(84.5% positive) and it has the most (35.7%) complaints about Product defects/faults.
5. Air conditioner is the category with the least positive reviews(74.4% positives) and it has the most (18.2%) complaints about customer service-related problems.
6. In the total negative reviews, we have 28.6% complaints about Faults in product and 8.93% complaints about Customer service issues.
7. product name - Whirlpool 7.5 kg Fully Automatic Top Load with In-built Heater Grey is most badly reviewed product.
8. Product name- Godrej 7 kg Fully Automatic Top Load with In-built Heater Grey is having more products faults.
9. Locations that are near the border of China, Nepal, Bhutan, and Bangladesh are having delayed delivery.

# Authors

- [@sumitsalve](https://github.com/sumitsalve98)


# 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://sumitsalve98.github.io/MyPortfolio/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sumit-salve-72b818217/)









