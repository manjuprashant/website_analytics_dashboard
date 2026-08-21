# Calculated Columns – Website Analytics (Sephora Dataset)

## Price Band

```DAX
Price Band =
SWITCH(
    TRUE(),
    sephora_website_dataset[price] < 25, "Budget",
    sephora_website_dataset[price] < 75, "Mid Range",
    sephora_website_dataset[price] < 150, "Premium",
    "Luxury"
)
```

## Rating Band

```DAX
Rating Band =
SWITCH(
    TRUE(),
    sephora_website_dataset[rating] < 3, "Low",
    sephora_website_dataset[rating] < 4, "Average",
    sephora_website_dataset[rating] < 4.5, "Good",
    "Excellent"
)
```

## Review Band

```DAX
Review Band =
SWITCH(
    TRUE(),
    sephora_website_dataset[number_of_reviews] < 100, "Low Reviews",
    sephora_website_dataset[number_of_reviews] < 1000, "Medium Reviews",
    "High Reviews"
)
```

## Love Band

```DAX
Love Band =
SWITCH(
    TRUE(),
    sephora_website_dataset[love] < 1000, "Low Interest",
    sephora_website_dataset[love] < 10000, "Medium Interest",
    "High Interest"
)
```

## Product Type

```DAX
Product Type =
IF(
    sephora_website_dataset[exclusive] = TRUE(),
    "Exclusive",
    "Regular"
)
```

## Online Availability

```DAX
Online Availability =
IF(
    sephora_website_dataset[online_only] = TRUE(),
    "Online Only",
    "Store & Online"
)
```

## Marketing Status

```DAX
Marketing Status =
IF(
    ISBLANK(sephora_website_dataset[MarketingFlags]),
    "No Campaign",
    "Marketing Campaign"
)
```

## Product Value Segment

```DAX
Product Value Segment =
SWITCH(
    TRUE(),
    sephora_website_dataset[value_price] <= sephora_website_dataset[price], "Standard",
    sephora_website_dataset[value_price] > sephora_website_dataset[price], "High Value"
)
```

## Limited Offer Status

```DAX
Limited Offer Status =
IF(
    sephora_website_dataset[limited_time_offer] = TRUE(),
    "Limited Offer",
    "Regular Offer"
)
```