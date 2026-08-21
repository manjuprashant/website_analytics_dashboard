# KPI Definitions

## Overview

This document defines all Key Performance Indicators used in the Sephora Website Analytics Dashboard.

---

## Total Products

### Definition

Total number of products available in the dataset.

### Formula

```DAX
COUNTROWS(sephora_website_dataset)
```

---

## Total Brands

### Definition

Total unique brands available.

### Formula

```DAX
DISTINCTCOUNT(sephora_website_dataset[brand])
```

---

## Total Categories

### Definition

Total unique product categories.

### Formula

```DAX
DISTINCTCOUNT(sephora_website_dataset[category])
```

---

## Average Rating

### Definition

Average customer rating across all products.

### Formula

```DAX
AVERAGE(sephora_website_dataset[rating])
```

---

## Total Reviews

### Definition

Total customer reviews across all products.

### Formula

```DAX
SUM(sephora_website_dataset[number_of_reviews])
```

---

## Total Loves

### Definition

Total customer "love" interactions.

### Formula

```DAX
SUM(sephora_website_dataset[love])
```

---

## Average Price

### Definition

Average selling price of products.

### Formula

```DAX
AVERAGE(sephora_website_dataset[price])
```

---

## Premium Products

### Definition

Products priced above $100.

### Formula

```DAX
price > 100
```

---

## Online Only Products

### Definition

Products available only through online channels.

### Formula

```DAX
online_only = TRUE()
```

---

## Exclusive Products

### Definition

Products marked as exclusive.

### Formula

```DAX
exclusive = TRUE()
```

---

## Limited Edition Products

### Definition

Products released as limited editions.

### Formula

```DAX
limited_edition = TRUE()
```

---

## Business Objectives

These KPIs help answer:

- Which brands are most popular?
- Which categories generate the highest engagement?
- What is the average product rating?
- Which products receive the most reviews?
- Which categories are premium-priced?
- How effective are marketing campaigns?