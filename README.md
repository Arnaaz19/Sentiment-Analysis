**Big Data Analysis of Twitter Sentiments: Insights from the 2020 US Presidential Election**

Abstract

This project employs advanced machine learning techniques to examine the correlation between Twitter sentiment during the 2020 US presidential election and actual election outcomes. By analyzing a meticulously curated dataset of election-related tweets, it provides profound insights into the influence of social media on political outcomes.

Introduction

Social media platforms like Twitter play a pivotal role in shaping political dialogue and public opinion. During the 2020 US Presidential Election, Twitter served as a hub for discourse and sentiment expression. This research leverages natural language processing (NLP) and machine learning to analyze the public sentiment expressed in tweets about the candidates and evaluate its potential to predict election results.

Data Sources

The analysis is based on two key datasets sourced from Kaggle:
	•	hashtag_donaldtrump.csv: Tweets tagged with #DonaldTrump.
	•	hashtag_joebiden.csv: Tweets tagged with #JoeBiden.

Data Preprocessing

Both datasets underwent rigorous preprocessing to ensure data quality:
	•	Removal of stopwords, emoticons, URLs, and other noise.
	•	Language detection to filter non-English tweets.
	•	Tokenization and normalization of text data.

Methodology

Sentiment Analysis
	•	Sentiments were categorized into positive, negative, and neutral using TextBlob.
	•	A custom machine learning model further refined the classification by reassigning neutral sentiments into positive or negative categories.

Machine Learning Approaches
	1.	Conventional Approach:
	•	Implemented using Spark’s MLlib for baseline comparison.
	2.	Custom Big Data Approach:
	•	A distributed machine learning model leveraging local computation to process large-scale data with enhanced fault tolerance and scalability.

Scalability and Fault Tolerance
	•	Scalability tested using linear size-up metrics.
	•	Fault tolerance is ensured by broadcasting models and predictions across nodes to recover from potential failures.

Results
	•	Sentiment Ratios:
	•	Positive tweets for Donald Trump: ~81.8%.
	•	Positive tweets for Joe Biden: ~85.4%.
	•	Key Insight: The sentiment ratio correlated strongly with the actual election outcomes, accurately predicting Joe Biden’s victory.
	•	The Custom Big Data Approach demonstrated superior fault tolerance and scalability compared to the conventional MLlib approach.



 Future Directions
	•	Enhance scalability by integrating state-level sentiment analysis.
	•	Leverage advanced distributed models such as Spark’s streaming API for real-time sentiment tracking.
	•	Incorporate additional data sources like news and polls for enriched analysis.

Contributors
	•	Harish Mohan Babu
 	•	Arnaaz Khan
	•	Saanidhya Khurana

License
This project is licensed under the MIT License. See the LICENSE file for details.
