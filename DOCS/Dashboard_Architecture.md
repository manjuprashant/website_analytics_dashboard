# Dashboard Architecture

## Project Name

Sephora Website Analytics Dashboard

---

# Architecture Overview

```text
Kaggle Sephora Dataset
           │
           ▼
      Power Query
           │
           ▼
    Data Cleaning
           │
           ▼
   Data Modeling Layer
           │
           ▼
    DAX Measures Layer
           │
           ▼
      Power BI Report
           │
           ▼
 Interactive Dashboard
```

---

# Data Flow

## Source Layer

Source:

- Kaggle Sephora Dataset

Contains:

- Product Information
- Pricing Information
- Customer Reviews
- Ratings
- Customer Loves
- Marketing Attributes

---

## Transformation Layer

Power Query operations:

- Remove duplicates
- Handle missing values
- Data type corrections
- Text standardization
- Feature engineering

Output:

Cleaned analytical dataset

---

## Data Modeling Layer

Primary table:

```text
sephora_website_dataset
```

Key dimensions:

- Brand
- Category
- Product Name

Measures:

- Product KPIs
- Engagement KPIs
- Pricing KPIs
- Marketing KPIs

---

## Report Layer

### Page 1

Website Analytics Overview

Visuals:

- KPI Cards
- Products by Category
- Top Brands
- Rating Distribution

---

### Page 2

Category Analysis

Visuals:

- Products by Category
- Average Rating by Category
- Average Price by Category
- Reviews by Category

---

### Page 3

Brand Analysis

Visuals:

- Top Brands
- Reviews by Brand
- Loves by Brand
- Average Rating by Brand

---

### Page 4

Customer Engagement Analysis

Visuals:

- Top Loved Products
- Most Reviewed Products
- Engagement by Category
- Rating vs Reviews

---

### Page 5

Pricing & Product Value Analysis

Visuals:

- Average Price by Category
- Average Price by Brand
- Price Distribution
- Price vs Rating

---

## Slicers

Dashboard-wide filters:

- Brand
- Category
- Online Only
- Exclusive
- Limited Edition
- Rating

---

## Expected Business Outcomes

The dashboard enables users to:

- Monitor product portfolio performance
- Analyze category growth opportunities
- Evaluate customer engagement
- Compare brand performance
- Understand pricing strategies
- Identify high-value products
- Support merchandising decisions