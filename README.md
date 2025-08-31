# Tweet Signal Pipeline 📈

A memory-efficient, modular NLP pipeline for converting Indian stock market tweets into quantitative trading signals using TF-IDF, sentiment analysis, and feature engineering.

# Technical Documentation

## Objective

Convert Indian stock market tweets into trading signals using NLP.

## Approach

1. **Cleaning & Preprocessing**
   - Unicode normalization (NFKC)
   - Punctuation and link removal
   - Supports Indian scripts (e.g., Devanagari)

2. **Feature Engineering**
   - TF-IDF: Top 1000 vector features
   - Sentiment: VADER lexicon
   - Keywords: Presence of "buy", "sell"
   - Composite: `sentiment + 0.5*buy - 0.5*sell`

3. **Visualization**
   - Sampling for plotting
   - Confidence bands (95%) via rolling STD

4. **Scalability**
   - Batch processing supported
   - Parquet for columnar, compressed storage
