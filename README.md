# Retail Sales Analysis Case Study

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.x-yellow.svg)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-green.svg)](https://matplotlib.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.x-orange.svg)](https://numpy.org/)

## Overview

This project analyzes retail sales data to evaluate the effectiveness of promotional campaigns and identify patterns in product performance across different stores. Using Python data analysis tools, the study segments products and stores into "Fast," "Medium," and "Slow" categories, quantifies promotional impact, and provides actionable insights for retail strategy optimization.

## Table of Contents

- [Retail Sales Analysis Case Study](#retail-sales-analysis-case-study)
  - [Overview](#overview)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Data Description](#data-description)
  - [Analysis Objectives](#analysis-objectives)
  - [Methodology](#methodology)
  - [Key Findings](#key-findings)
  - [Visualizations](#visualizations)
  - [Conclusions](#conclusions)
  - [Requirements](#requirements)
  - [Usage](#usage)

## Introduction

Retail promotions are a vital component of sales strategy, but their effectiveness can vary significantly across products and stores. This case study examines a comprehensive dataset of retail sales spanning multiple months, with a focus on analyzing how different products and stores respond to promotional periods.

## Data Description

The analysis uses the `veriler.xlsx` file containing the following sheets:
- `assignment4-1a`: Contains daily sales data with columns:
  - `Date`: Transaction date
  - `StoreCode`: Unique store identifier
  - `ProductCode`: Unique product identifier
  - `SalesQuantity`: Number of units sold
- `PromotionDates`: Contains information about promotional periods:
  - Promotion name (Promo1, Promo2, etc.)
  - Start and end dates for each promotion

Dataset scope:
- Time period: January 2015 - May 2015
- 340 unique stores
- Hundreds of unique products
- Over 1 million sales records

## Analysis Objectives

1. Identify which products experienced the greatest sales increases during promotional periods
2. Determine if certain stores show stronger responses to promotions
3. Compare the promotional response between fast-selling and slow-selling products
4. Analyze the effectiveness of different promotional periods
5. Provide data-driven insights for optimizing future promotional strategies

## Methodology

1. **Data Preparation**:
   - Loading and cleaning the sales and promotion data
   - Converting dates to proper datetime format
   - Handling missing values and verifying data integrity

2. **Sales Categorization**:
   - Classifying products as "Fast," "Medium," or "Slow" based on weekly sales metrics
   - Categorizing stores using quantile-based segmentation

3. **Promotional Impact Analysis**:
   - Calculating average sales during promotional and non-promotional periods
   - Measuring sales lift for each product-store combination
   - Identifying products with the highest promotion response

4. **Store Response Analysis**:
   - Evaluating store-level promotional effectiveness
   - Comparing response patterns across store categories

5. **Visualization**:
   - Creating bar charts for promotion vs. non-promotion periods
   - Visualizing top-performing products during promotions
   - Illustrating store-level promotion response

## Key Findings

1. **Promotional Effectiveness**:
   - Overall, promotions increased average weekly sales by approximately 9.5% (from 3.12 to 3.41 units)
   - Product 137 showed the most consistent high response to promotions across multiple stores

2. **Top Performing Products**:
   - Product 137 experienced the largest sales increase during promotions, with some stores showing a 70-unit increase
   - Products 137 and 139 dominated the top 10 list of highest promotional lifts

3. **Store Response Patterns**:
   - Stores 184, 268, and 301 showed the strongest positive responses to promotions
   - Some stores (particularly 130, 324, and 121) actually performed worse during promotional periods

4. **Category Insights**:
   - Fast products: 6.03 avg. sales during promotions vs. 6.87 during non-promotional periods
   - Medium products: 1.48 avg. sales during promotions vs. 1.59 during non-promotional periods
   - Slow products: 0.52 avg. sales during promotions vs. 0.40 during non-promotional periods

5. **Store Category Analysis**:
   - Fast stores: 4.99 avg. sales during promotions vs. 4.85 during non-promotional periods
   - Medium stores: 2.95 avg. sales during promotions vs. 2.91 during non-promotional periods
   - Slow stores: 2.01 avg. sales during promotions vs. 1.93 during non-promotional periods

## Visualizations

The analysis includes several visualizations:
- Bar charts comparing promotional and non-promotional sales periods
- Time series plots showing sales during each promotion
- Comparative analysis of store performance during promotions
- Product performance charts highlighting promotional impact

## Conclusions

1. **Targeted Promotion Strategy**:
   - Focus promotional efforts on Product 137, which consistently shows the strongest response
   - Prioritize promotions in high-response stores like 184, 268, and 301

2. **Promotion Effectiveness by Category**:
   - Slow-moving products show the most significant percentage increase during promotions
   - Fast-moving products may not need promotional support as much as slower-moving ones

3. **Store Optimization**:
   - Consider reducing or eliminating promotions in stores showing negative responses
   - Implement store-specific promotional strategies based on historical response patterns

4. **Future Recommendations**:
   - Test more targeted promotions for specific product-store combinations
   - Consider different promotional mechanics for different product categories
   - Implement a more rigorous A/B testing approach for future promotional campaigns

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- openpyxl

## Usage

1. Ensure the required dependencies are installed:
```bash
pip install pandas matplotlib numpy openpyxl
```

2. Place the `veriler.xlsx` file in the same directory as the analysis script

3. Run the analysis script:
```bash
jupyter retail_analysis.ipynb
```

4. Review the generated visualizations and analysis output