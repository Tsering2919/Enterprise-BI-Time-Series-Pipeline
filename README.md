# Enterprise Business Intelligence & Time Series Forecasting Pipeline

## The Business Problem
To make proactive operational and marketing decisions, businesses need to accurately understand customer engagement patterns, predict future interaction volumes, and drive loyalty through personalized recommendations. This project provides an end-to-end data pipeline that ingests raw, unstructured customer review data and translates it into predictive insights and actionable business intelligence.

## Key Performance Outcomes
* **Big Data Processing:** Architected a distributed data wrangling pipeline using PySpark to ingest, clean, and format over 552,000 raw customer records, enabling scalable downstream analytics[cite: 3].
* **Time Series Forecasting:** Conducted a grid search across 27 configurations to build an optimal ARIMA (0,1,1) forecasting model, achieving a highly accurate Mean Absolute Error (MAE) of 38.08 for 30-day short-term volume predictions[cite: 3].
* **Recommendation Engine:** Deployed a K-Nearest Neighbors (KNN) Collaborative Filtering recommendation system utilizing cosine similarity, effectively navigating a 99.5% sparse utility matrix to align user preferences[cite: 3].
* **Automated Data Extraction (OCR):** Engineered a document processing workflow using Tesseract OCR and Regex to automatically parse unstructured PDF strategy reports into structured, quantitative year-over-year DataFrames[cite: 3].
* **NLP & Sentiment Analysis:** Applied custom stopword filtering and frequency tracking to extract core customer complaint themes and track sentiment ratios (5.28 Positive/Negative) across multiple business categories[cite: 3].

## Technical Architecture
* **Data Processing & ETL:** PySpark, Pandas, NumPy[cite: 3]
* **Machine Learning & AI:** Scikit-learn (KNN), SciPy[cite: 3]
* **Time Series Modeling:** Statsmodels (ARIMA, Seasonal Decomposition)[cite: 3]
* **Natural Language Processing (NLP):** WordCloud, Regular Expressions (Regex)[cite: 3]
* **Computer Vision / OCR:** Pytesseract, pdf2image[cite: 3]
* **Data Visualization:** Matplotlib, Seaborn[cite: 3]

## Project Structure
* `notebook.ipynb`: The primary executable Jupyter Notebook containing the full ETL, analysis, modeling, and OCR pipeline.
* `sample_data.csv`: A truncated sample of the original customer dataset to demonstrate the starting schema without exposing the full massive raw file.
* `requirements.txt`: The library dependencies required to reproduce this environment.

## Reproducibility
To run this pipeline locally, clone the repository and install the required dependencies:
```bash
pip install -r requirements.txt

(Note: To execute the OCR components, you must have Tesseract-OCR and Poppler-utils installed on your local machine/server.)
