# Stock-Price-Prediction-using-Twitter-Sentiment-Analysis

## Project Overview
This project explores the relationship between social media sentiment and stock market movements by analyzing Twitter data and historical stock prices. Using machine learning techniques, we predict stock price movements based on public sentiment expressed through tweets, specifically focusing on HDFC Bank as a case study.

## Key Features
- Real-time Twitter data collection and sentiment analysis
- Historical stock price data integration using Yahoo Finance API
- Advanced data preprocessing and feature engineering
- Neural network-based prediction model
- Interactive data visualization

## Technical Implementation

### Data Collection
- **Twitter Data**: Leverages Twitter API (via Tweepy) to gather tweets containing #HDFC
- **Stock Data**: Utilizes yfinance library to fetch historical stock prices
- **Time Period**: 9-day analysis window (constrained by Twitter API limitations)

### Data Processing Pipeline
1. **Twitter Data Preprocessing**
   - Text cleaning (removing mentions, hashtags, URLs)
   - Sentiment analysis using TextBlob
   - Polarity scoring (-1 to 1 scale)
   - Subjectivity analysis

2. **Stock Data Engineering**
   - Calculated features:
     - High-Low Percentage (HLPCT) = (High-Low)/High
     - Percentage Change (PCTchange) = (Close-Open)/Open
   - Adjusted Close price normalization
   - Volume analysis
   - Handling market closure days through interpolation

### Machine Learning Model
- **Feature Matrix Components**:
  - Tweet sentiment polarity
  - Adjusted Close price
  - HLPCT
  - PCTchange
  - Trading volume

- **Model Architecture**:
  - Neural network implementation using TensorFlow/Keras
  - 80-20 train-test split
  - Linear regression as base model
  - Extensible to polynomial regression with cross-validation

### Visualization
- Word cloud generation for tweet content analysis
- Time-series plots of sentiment polarity
- Stock price movement visualization
- Sentiment vs. stock price correlation analysis

## Technical Stack
- Python 3.x
- Libraries:
  - Tweepy (Twitter API)
  - TextBlob (Sentiment Analysis)
  - yfinance (Stock Data)
  - TensorFlow/Keras (ML Model)
  - Pandas & NumPy (Data Processing)
  - Matplotlib (Visualization)
  - WordCloud (Text Analysis)

## Note
This project serves as a proof of concept for sentiment-based stock prediction. While the model provides insights into market sentiment, it should not be used as the sole basis for investment decisions.
