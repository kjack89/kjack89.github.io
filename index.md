---
title: '**Data Analysis and Visualization Projects**'
geometry: margin=2
output:
  html_document:
    theme: cosmo
    toc: yes
    toc_float: yes
    includes:
      in_header:
  pdf_document:
    toc: yes
---

<style type="text/css">

div {
color: #170279;
}

#TOC {
  color: #27B789;
}

.list-group-item.active, .list-group-item.active:focus, .list-group-item.active:hover {
  color: #27B789;
  background-color: #4127B7;
}

a:link {
    color: #27B789;
    text-decoration: none;
}

a:visited {
        text-decoration: none;
color: #27B789;

}
a:hover {
color: #27B789;
background-color: #4127B7;
}

.main-container {
  max-width: 300px;
  margin-left: auto;
  margin-right: auto;
}

.column {
  float: left;
  width: 50%;
}

.row:after {
  content: "";
  display: table;
  clear: both;
} 

</style>

Hello, and welcome. This website serves as a place to showcase projects that I have worked on. Working on personal projects is how I apply things that I have learned, and also how I learn new things. Feel free to reuse anything you find here. If you find something that you don't like, or find something that could be done better, and would like to tell me, **[please email me](<mailto:kevinjdswork@gmail.com>)**. New projects are on the horizon, as time permits. Thank you for stopping by.



# **Interactive Pallet Tracking Dashboard in R**
________________________________________________
* **[Go to the Repository.](https://github.com/kjack89/palletDashboard)**
## Overview

Used RShiny and Leaflet maps to provide a vanilla interactive dashboard for longitude/latitude logistics data. This particular implementation illustrates where approximately 40 different assets/objects have moved over time. Simple metrics, options to view specific assets/objects, and date filtering are all included on the dashboard.

<img src="palletMap.png" width="740px" height="auto">



# **Analyzing Webscraped Craigslist Car Ads in Python**
_______________________________________________________
* **[Go to the Repository.](https://github.com/kjack89/carAdAnalysis)**

## Overview

## Gathering the Data

**[view code](https://github.com/kjack89/carAdAnalysis/blob/master/webScrapeCarData.py)**

Used BeautifulSoup and Selenium to extract data from Craigslist car ads and fueleconomy.gov. The data extracted from Craiglist includes text information contained in the body of each ad, requiring the script to navigate to each individual ad to extract this information. This makes the script take approx. 24-30 hours to complete since it depends on network protocol speeds to get the data from each ad. In this particular unprocessed dataset, there are about 320,000 entries for car and truck ads.

## Cleaning and Preprocessing

**[view code (1st cleaning pass)](https://github.com/kjack89/carAdAnalysis/blob/master/cleanCarsFirstPass.py)**

**[view code (2nd cleaning pass)]()**

As was expected, Craigslist data is very messy with lots of missing values, misspelled entries, innaccurate values, etc. The first round of cleaning fills in or corrects values based off of the ad's title and body text. I viewed this as the most 'accurate' representation of the data, since it comes directly from the source. In the second round of cleaning I used machine learning algorithms to impute missing values for the categorical features. I compared model accuracies between XGBoost, K-nn, and SVM. XGBoost performed the best, however I did not spend much time parameter tuning the models. The little I did do only provided very small differences in model accuracy. The continuous variables were imputed using the median.

| label |
|------|
| price |

| feature | description |
|------|---------|
| city |  listed city from craiglist search. craigslist merges some cities together. |
| state |  state |
| date | mm/dd/yy  |
| time | time of day of posting  |
| altloc | location posted on ad, may differ from city.  |
| condition | **categorical**:  'new' ,'like new', 'excellent', 'good', 'fair', 'salvage', 'as new'|
| cylinders | number of cylinders, **categorical**: '3' ,'4', '6', '5', '8', '10', '12', 'other'|
| drive | **categorical**: 'fwd', '4wd', 'rwd'|
| fuel | fuel type, **categorical**: 'gas', 'hybrid', 'diesel', 'electric', 'petrol', 'other'| 
| odometer |  **continuous** | 
| size |  **categorical**: 'compact', 'full-size', 'mid-size', 'sub-compact', 'small family car'| 
| title status | **categorical**: 'clean', 'salvage', 'rebuilt', 'lien', 'parts only', 'missing'|
| transmission | **categorical**: 'manual', 'automatic', 'other'|
| type | **categorical**: 'hatchback', 'SUV', 'sedan', 'convertible', 'van', 'mini-van', 'truck', 'pickup', 'coupe', 'wagon', 'offroad', 'other', 'suv', 'bus', 'saloon'|
| make | **categorical**, based off cars from fueleconomy.gov from 1984-present|
| model | **categorical**, based off cars from fueleconomy.gov from 1984-present|
| year | 1984-present |

## Exploratory Analysis

## Final Analysis



# **Another Project Coming Soon**
_________________________________
* **[Go to the Repository.]()**

## Overview

This page was last updated on `r Sys.time()` Eastern Time.
