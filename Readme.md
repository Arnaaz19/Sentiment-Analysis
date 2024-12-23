# Unveiling Twitter Sentiments: A Big Data Dive into Twitter Sentiments during the 2020 US Elections

## Abstract
This project employs advanced machine learning techniques to examine the correlation between Twitter sentiment during the 2020 US presidential election and actual election outcomes. Analyzing a meticulously curated dataset of election-related tweets offers profound insights into social media's impact on political outcomes.

## Introduction
Social media platforms like Twitter significantly shape political dialogue. This research analyzes Twitter discourse from the 2020 US Presidential Election, employing natural language processing (NLP) and machine learning to decipher public sentiment and evaluate its influence on electoral results.

## Data Sources
The analysis is based on two main datasets sourced from Kaggle:
- `hashtag_donaldtrump.csv`: Tweets tagged with #DonaldTrump.
- `hashtag_joebiden.csv`: Tweets tagged with #JoeBiden.

These datasets underwent extensive preprocessing to ensure the data quality for sentiment analysis.

## Notebooks and Execution Order
The project comprises several notebooks, each serving a specific function in the research pipeline. To replicate our findings or further explore the data, please execute the notebooks in the following order:

1. **Twitter Sentiment Analysis_V1_Trump**
   - Uses TextBlob to analyze sentiments from tweets about Donald Trump.
   
2. **Twitter Sentiment Analysis_V1_Biden**
   - Uses TextBlob to analyze sentiments from tweets about Joe Biden.
   
3. **Regular ML Solution Combined_mllib**
   - Implements a standard machine learning approach using Spark MLlib to benchmark the performance of the sentiment analysis.
   
4. **Custom ML Solution Combined**
   - Deploys a custom Big Data machine learning model designed to refine sentiment classifications further and compare against the regular ML approach.

## Required Libraries and Installation
This project relies on several Python libraries and Spark ML packages. Ensure these are installed by running the following commands:


%pip install nltk
%pip install pandas
%pip install seaborn
%pip install matplotlib
%pip install wordcloud
%pip install pyspark==3.0.1 # Adjust the version based on your Spark installation
%pip install textblob
%pip install langdetect
%pip install wordninja

The following Python and PySpark libraries are used throughout the notebooks:
from pyspark.sql import SparkSession
import matplotlib.pyplot as plt
import seaborn as sns
import pyspark.sql.functions as F
from nltk.corpus import stopwords
from nltk.stem import WordNetLemmatizer
import re
import pandas as pd

Detailed import statements and specific library uses can be found at the top of each notebook.

## Methodology
Data Collection
Data was collected from publicly available Kaggle datasets, focusing on tweets from key periods of the election cycle.

## Data Preprocessing
Tweets were preprocessed to remove noise such as stopwords, emoticons, and URLs to prepare them for accurate sentiment analysis.

## Sentiment Analysis
Sentiments were categorized into positive, negative, and neutral using TextBlob. This classification was crucial for preparing the data for deeper analysis.

## Machine Learning
The analysis featured two machine learning methodologies:

A conventional model using Spark’s MLlib for a baseline comparison.
An advanced custom model that leverages local distributed Big Data approaches for enhanced analysis.
Results
The research identified a strong correlation between Twitter sentiment and the actual outcomes of the elections, suggesting Twitter’s potential utility as a predictive tool for electoral behavior under specified conditions.

## Conclusion
Our findings underscore the significant influence of social media sentiment on political dynamics, positioning Twitter as a potential predictive tool for election outcomes. Future studies could delve into more detailed regional sentiment analysis or integrate additional social media platforms to broaden these insights.

How to Use This Repository
To use this repository:

Clone the repository to your local machine.
Ensure you have Python and necessary libraries installed.
Execute the Jupyter notebooks in the order specified above to replicate the analysis or explore the data further.