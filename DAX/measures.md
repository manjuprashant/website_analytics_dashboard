# DAX Measures – Website Analytics (Sephora Dataset)

## Total Products

```DAX
Total Products =
COUNTROWS(sephora_website_dataset)
```

## Total Brands

```DAX
Total Brands =
DISTINCTCOUNT(sephora_website_dataset[brand])
```

## Total Categories

```DAX
Total Categories =
DISTINCTCOUNT(sephora_website_dataset[category])
```

## Average Rating

```DAX
Average Rating =
AVERAGE(sephora_website_dataset[rating])
```

## Total Reviews

```DAX
Total Reviews =
SUM(sephora_website_dataset[number_of_reviews])
```

## Total Loves

```DAX
Total Loves =
SUM(sephora_website_dataset[love])
```

## Average Price

```DAX
Average Price =
AVERAGE(sephora_website_dataset[price])
```

## Maximum Price

```DAX
Maximum Price =
MAX(sephora_website_dataset[price])
```

## Minimum Price

```DAX
Minimum Price =
MIN(sephora_website_dataset[price])
```

## Average Value Price

```DAX
Average Value Price =
AVERAGE(sephora_website_dataset[value_price])
```

## Products Count

```DAX
Products Count =
COUNTROWS(sephora_website_dataset)
```

## Reviews Count

```DAX
Reviews Count =
SUM(sephora_website_dataset[number_of_reviews])
```

## Loves Count

```DAX
Loves Count =
SUM(sephora_website_dataset[love])
```

## Avg Loves Per Product

```DAX
Avg Loves Per Product =
DIVIDE(
    SUM(sephora_website_dataset[love]),
    COUNTROWS(sephora_website_dataset),
    0
)
```

## Premium Products

```DAX
Premium Products =
COUNTROWS(
    FILTER(
        sephora_website_dataset,
        sephora_website_dataset[price] > 100
    )
)
```

## Online Only Products

```DAX
Online Only Products =
CALCULATE(
    COUNTROWS(sephora_website_dataset),
    sephora_website_dataset[online_only] = TRUE()
)
```

## Exclusive Products

```DAX
Exclusive Products =
CALCULATE(
    COUNTROWS(sephora_website_dataset),
    sephora_website_dataset[exclusive] = TRUE()
)
```

## Limited Edition Products

```DAX
Limited Edition Products =
CALCULATE(
    COUNTROWS(sephora_website_dataset),
    sephora_website_dataset[limited_edition] = TRUE()
)
```