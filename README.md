# Skincare Product Text Analytics Project 🥝

## Overview
This repository contains our text analytics project focused on skincare product reviews and analysis. Our project won recognition for Most Effective Visualizations in the course presentation. The research combines Amazon review data with Reddit discussions to build a comprehensive recommendation system based on skin concerns and consumer sentiment.
With this project we work on what was learnt in class, and try to apply text analytics to a real business use-case, Big-Data user research and advertisement. What if you could figure out the ideal product for each user based on how they engage in online discourse? 

## Key Visualizations
1. **Word Prediction Analysis**
   - Scatter plot showing words that predict review ratings
   - X-axis: coefficient values indicating predictive power
   - Y-axis: word frequency in reviews
   - Notable finding: Stronger indicators for negative reviews than positive ones
<img src="https://github.com/laurazecca01/text-analytics-skincare/blob/main/images/rundown%20of%20the%20topic%20modelling%20results.png?raw=true" alt="Scatterplot" width="400"/>
2. **Word Clouds**
   - Reviews cloud: More verb-focused (love, make, try, put, smell, buy)
   - Description cloud: More noun-focused (formula, fragrance, moisturizer, oil, face)
   - Common terms in both: "product" and "skin"
<img src="https://github.com/laurazecca01/text-analytics-skincare/blob/main/images/wordcloud%20n2.png?raw=true" alt="WordClouds" width="400"/>
3. **Topic Modeling Networks**
   - Visualizes relationships between skincare concerns and product types
   - Each node represents either a topic or highly relevant terms
   - Connections show shared terminology between topics

<img src="https://github.com/laurazecca01/text-analytics-skincare/blob/main/images/rundown%20of%20the%20topic%20modelling%20results-1.png?raw=true" alt="Topic Modeling Results" width="400"/>


## Methodology

### Data Preparation
1. **Data Collection & Cleaning**
   - Merged product data using PSQL
   - Filtered for:
     - Average review rating > 3
     - Word count > 150 words
     - Minimum 300 reviews
   - Created unified product description column

2. **Text Processing**
   - Stopword removal using spaCy
   - Lemmatization of product descriptions and reviews
   - Punctuation removal
   - TAB dfm function implementation for document feature matrix

### Analysis Components

1. **Rating Prediction Model**
   - Built using review text data
   - Implemented VADER sentiment analysis
   - Calculated average sentiment scores per product

2. **Topic Modeling**
   - Applied NMF matrix to both product descriptions and reviews
   - Identified key skin concerns and product categories
   - Created weighted scoring system for skin concerns

3. **Recommendation System**
   - Built on topic modeling results
   - Incorporates sentiment scores
   - Can filter by product type and skin concern
   - Network visualization-based topic selection

4. **Cross-Platform Analysis**
   - Compared Amazon reviews vs Reddit discussions
   - Analyzed r/SkincareAddicts topics
   - Vector similarity matching between questions and products

## Repository Structure
- `Main.html` - Primary research findings and analysis
- `Lasso_model.html` - Implementation and results of our Lasso regression model
- `topic_network_1.html` & `topic_network_2.html` - Interactive topic modeling visualizations

## Languages Used
- Python (spaCy, VADER, NMF)
- R
- SQL

## Contributors
Sofiana Milo
Laura Zecca
Aoife Lagan
Ana Rodrigo De Pablo
