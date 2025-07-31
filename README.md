News Sentiment Analysis
This project builds a machine learning model to perform sentiment analysis on financial news headlines using Python libraries like transformers and feedparser. The model is based on pre-trained language models and demonstrates fetching data from an RSS feed, text processing, and sentiment classification.

Objective
The objective is to fetch recent financial news headlines for a given stock ticker and keyword, then analyze the sentiment of these headlines to provide an overall sentiment score (positive, negative, or neutral).

Technologies Used
Python

feedparser

transformers

torch

pandas

bottleneck

Dataset
The dataset is a live RSS feed of top financial headlines from Yahoo Finance. The script fetches entries for a specified ticker (e.g., GC=F for Gold Futures) and a keyword (e.g., 'gold').

The data includes:

title – The headline of the news article

link – The URL to the full article

published – The publication date and time

summary – A brief summary of the article

Steps Performed
Environment Setup: Imports necessary libraries and initializes a sentiment analysis pipeline using a pre-trained model like ProsusAI/finbert.

Model Demonstration: A sample sentence is passed to the pipeline to confirm the model's functionality.

News Feed Parsing: The script fetches news entries from a Yahoo Finance RSS feed for a specified ticker and keyword.

Sentiment Analysis: It iterates through the fetched entries and uses a sentiment analysis model to determine the sentiment (positive or negative) and a corresponding score for each relevant article's summary. The code also mentions using distilbert-base-uncased-finetuned-sst-2-english as a model.

Score Aggregation: The scores from individual articles are aggregated to calculate a final overall sentiment score.

Overall Sentiment Classification: Based on the final score, the overall sentiment is classified as "positive," "negative," or "neutral". For example, a final score of 0.7481 is classified as "positive".

Results
The project successfully fetches and analyzes financial news, providing an overall sentiment for a specific asset.

Files Included
sentiment_analysis.ipynb – Jupyter notebook with the full implementation.
