# Data Cleaning Process

## Project Overview

The Sephora Website Analytics Dashboard was developed using the Sephora product dataset obtained from Kaggle. The dataset contains product information, pricing details, customer ratings, reviews, engagement metrics, and promotional attributes.

---

## Dataset Fields

The dataset includes the following key columns:

- id
- brand
- category
- name
- size
- rating
- number_of_reviews
- love
- price
- value_price
- URL
- MarketingFlags
- MarketingFlags_content
- options
- details
- how_to_use
- ingredients
- online_only
- exclusive
- limited_edition
- limited_time_offer

---

## Data Cleaning Steps

### Step 1 – Import Dataset

- Downloaded dataset from Kaggle
- Loaded CSV file into Power BI Desktop
- Verified column names and data types

### Step 2 – Remove Duplicates

Removed duplicate products using:

- id
- product name
- brand

Power Query:

```PowerQuery
Remove Duplicates
```

---

### Step 3 – Handle Missing Values

Checked for null values in:

- rating
- number_of_reviews
- love
- price
- value_price

Actions:

- Replaced null numeric values with 0 where appropriate
- Removed records with missing product identifiers

---

### Step 4 – Data Type Validation

Converted columns to proper data types.

| Column | Data Type |
|----------|----------|
| id | Whole Number |
| brand | Text |
| category | Text |
| name | Text |
| rating | Decimal Number |
| number_of_reviews | Whole Number |
| love | Whole Number |
| price | Decimal Number |
| value_price | Decimal Number |

---

### Step 5 – Text Standardization

Applied transformations:

- Trim spaces
- Clean text
- Standardize category names
- Standardize brand names

---

### Step 6 – Feature Engineering

Created calculated columns:

- Price Band
- Rating Band
- Review Band
- Love Band
- Marketing Status
- Product Value Segment

---

### Step 7 – Data Validation

Validated:

- Total products
- Brand counts
- Category counts
- Price ranges
- Ratings distribution

---

## Final Dataset Readiness

The cleaned dataset is ready for:

- Product Analytics
- Category Analysis
- Brand Analysis
- Customer Engagement Analysis
- Pricing Analysis
- Marketing Analysis