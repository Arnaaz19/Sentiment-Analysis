**Big Data Analysis of Twitter Sentiments: Insights from the 2020 US Presidential Election**

Overview

This project explores a big data approach to analyze Twitter sentiments during the 2020 US presidential election. Using distributed computing techniques and machine learning models, it investigates the correlation between social media sentiments and real-world election outcomes. The project emphasizes scalability, fault tolerance, and performance efficiency, making it a robust example of leveraging big data methodologies for large-scale sentiment analysis.

Objectives
	•	Develop a scalable big data pipeline for analyzing millions of tweets.
	•	Perform sentiment classification (positive, negative, neutral) using TextBlob and enhance it by reclassifying neutral sentiments with custom machine learning models.
	•	Compare performance and fault tolerance between the custom big data approach and Apache Spark MLlib.
	•	Validate the relationship between sentiment ratios and election results.

Key Features
	1.	Big Data Approach:
	•	Distributed model training and prediction using worker nodes.
	•	Fault-tolerant ensemble techniques for handling large-scale data.
	•	Scalable pipeline proven through linear size-up testing.
	2.	Sentiment Analysis:
	•	TextBlob for initial sentiment classification.
	•	Logistic Regression models to reclassify neutral sentiments into positive or negative categories.
	•	Integration of distributed computing to process and aggregate results efficiently.
	3.	Prediction and Validation:
	•	Sentiment ratios of positive tweets for Donald Trump and Joe Biden analyzed.
	•	Model accurately predicted Joe Biden’s victory.

Data

The dataset, sourced from Kaggle, includes:
	•	Over 2 million tweets for Donald Trump.
	•	Approximately 1.8 million tweets for Joe Biden.
	•	Features such as tweet text, timestamps, and preprocessed sentiment scores.

Data Preprocessing
	•	Removed non-textual elements like emojis, hashtags, and URLs.
	•	Converted all text to lowercase and filtered out non-English tweets.
	•	Applied robust NLP techniques to refine the dataset for sentiment analysis.

Methodology

Custom Big Data Approach
	1.	Data Distribution:
	•	Tweets split across worker nodes for parallel processing.
	2.	Model Training:
	•	Logistic Regression models trained locally on each node using distributed datasets.
	3.	Ensemble Predictions:
	•	Majority voting mechanism aggregated predictions from multiple nodes for robustness.
	4.	Fault Tolerance:
	•	Models and predictions broadcast across nodes to recover from failures.

Model Comparison
	•	Spark MLlib Logistic Regression:
	•	Standard sequential processing model.
	•	Custom Big Data Approach:
	•	Distributed model leveraging local computation on multiple nodes.

Scalability Testing
	•	Tested runtime for processing 10%, 20%, and 100% of the data.
	•	Results showed near-linear scalability of the big data pipeline.

Results
	1.	Sentiment Ratios:
	•	Positive Sentiments (including reclassified neutrals):
	•	Donald Trump: ~81.8%
	•	Joe Biden: ~85.4%
	•	Biden’s higher positive sentiment ratio accurately predicted his victory.
	2.	Performance Metrics:
	•	Custom Big Data Approach achieved:
	•	Slightly lower Mean Absolute Error (MAE) compared to Spark MLlib.
	•	Fault tolerance and enhanced robustness in distributed environments.
	3.	Scalability:
	•	Linear scalability demonstrated through runtime testing with different data sizes.

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
