# Zepto Data Pipeline — Module 1

## Overview

This project implements a raw-to-relational data pipeline for catalog-style product pricing and availability analysis.

The pipeline uses the public `books.toscrape.com` website as the data source and performs the following workflow:

Scrape → Clean → Convert → Store → Query → Validate

The project demonstrates web scraping, data cleaning, currency conversion, relational database design, SQL analysis, and pandas-based validation.

---

## Data Source

Source website:

https://books.toscrape.com/

The website is a public scraping-practice site and does not require:

- Login
- API key
- Paid subscription

The pipeline scrapes books across multiple categories and pagination pages.

Final dataset contains at least 60 books across at least 3 categories.

---

## Project Structure

```text
data_pipeline/
│
├── data/
│   ├── raw_books.csv
│   ├── cleaned_books.csv
│   └── books.db
│
├── outputs/
│   ├── query1_price_above_40.csv
│   ├── query2_top10_expensive.csv
│   ├── query3_categories.csv
│   ├── query4_price_between_20_30.csv
│   ├── query5_selected_categories.csv
│   ├── query6_join_books_categories.csv
│   ├── pandas_merge_join_result.csv
│   └── sql_queries.txt
│
├── data_pipeline.ipynb
├── requirements.txt
└── README.md