# Financial News Sentiment Analysis

This project performs sentiment analysis on financial news headlines using Python and Hugging Face's Transformers. It fetches news headlines from Yahoo Finance RSS feeds based on a given stock ticker and uses a pretrained model to classify the sentiment of each headline as positive, negative, or neutral.

## Objective

Analyze recent news articles related to a specific stock (e.g., META, AAPL, TSLA) and determine the overall sentiment to assist with investor decision-making.

## Technologies Used

- Python  
- Feedparser  
- Transformers (Hugging Face)  
- Pretrained Model: `distilbert-base-uncased-finetuned-sst-2-english`  
- Jupyter Notebook  

## Data Source

News headlines are fetched from Yahoo Finance using RSS feeds. The URL is constructed based on the stock ticker provided by the user.

## Steps Performed

### Data Retrieval
- Parsed RSS feed from Yahoo Finance using `feedparser`
- Extracted titles, publication dates, and summaries

### Preprocessing
- Filtered articles based on presence of the stock keyword
- Cleaned and prepared text summaries

### Sentiment Analysis
- Used Hugging Face Transformers pipeline
- Applied sentiment classification on each news summary

### Scoring
- Assigned positive or negative scores based on sentiment
- Calculated average sentiment score
- Determined overall sentiment (positive / negative / neutral)

## Results

- Successfully analyzed news sentiment for the given stock
- Printed sentiment for each relevant article
- Computed an overall sentiment score across all matched articles

## Files Included

- `sentiment_analysis.ipynb` – Jupyter Notebook with full implementation

## Future Work

- Add time-based sentiment trend visualizations
- Support more NLP models for comparison
- Export results to CSV or JSON
- Build a web interface using Streamlit or Flask
