# Stock Movement Analysis Based on Social Media Sentiment

## **Project Overview**
This project predicts stock movements based on sentiment analysis of Reddit posts from the `r/stocks` subreddit. Using Natural Language Processing (NLP) and machine learning, it extracts insights from user-generated content, processes the data, and forecasts stock trends.

---

## **Features**
1. **Data Collection**  
   - Scrapes posts from `r/stocks` using the Reddit API.
   - Collects titles, post bodies, scores, comments, and timestamps.

2. **Data Preprocessing**  
   - Cleans text by removing noise (e.g., URLs, punctuation) and stopwords.
   - Tokenizes and normalizes text data.

3. **Sentiment Analysis**  
   - Calculates sentiment polarity using VADER.
   - Sentiment scores for titles and bodies are extracted.

4. **Feature Engineering**  
   - Extracts stock mentions, post scores, and sentiment scores.
   - Combines Reddit data with historical stock price data.

5. **Machine Learning Models**  
   - Trains Logistic Regression and Random Forest Classifier to predict stock movement.
   - Evaluates model performance with metrics like accuracy, precision, and recall.

---
## Setup Instructions
1. Create a `.env` file in the project root.
2. Add the following environment variables:
REDDIT_CLIENT_ID=your_client_id_here
REDDIT_CLIENT_SECRET=your_client_secret_here
REDDIT_USER_AGENT=your_user_agent_here


## **Project Structure**
```
.
├── data/                                  # Contains raw and processed data
│   ├── reddit_stocks.csv
│   ├── reddit_stocks_with_sentiment.csv
│   ├── reddit_stocks_features.csv
│   ├── historical_stock_prices.csv
│
├── scripts/main.py                       # Python scripts for each step
│   ├── reddit_scraper                    # Scrapes Reddit data
│   ├── preprocess_data                   # Preprocesses and cleans text data
│   ├── sentiment_analysis                # Performs sentiment analysis
│   ├── feature_engineering               # Extracts features for training
│   ├── model_training                    # Trains machine learning models
│
├── results/                              # Results and outputs
│   ├── trained_model                     # Trained Random Forest model
│   ├── evaluation_metrics                # Model performance metrics
│
├── README.md                            # Project documentation
└── report.pdf                           # Detailed report
```
