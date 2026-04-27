# SQL_project - Analyzing olimit ecommerce data

# Olist Brazilian Ecommerce — Analysis

## Project Goal
Analyze 100,000+ orders to understand delivery delays and product performance for an ecommerce company operating across Brazil's 26 states.

## Data Source
Public dataset from Olist (Kaggle): 8 tables including orders, customers, sellers, products, and payments.

## Key Business Questions Answered

### 1. Which product categories sell the most?
- **Top category:** bed_bath_table (11,115 items sold)
- **Second:** health_beauty (9,670 items sold)
- **Third:** sports_leisure (8,641 items sold)

### 2. How often are deliveries late?
- **Late delivery rate:** 7.87% of all completed orders
- **On-time delivery rate:** 89.15%

### 3. Which state routes have the worst delays?
- **Worst route:** AM → AL (38 days average delay, excluding one outlier)
- **Second worst:** BA → AC (24 days)
- **Insight:** Routes to North region (AM, AC, RR) consistently show 5+ day delays regardless of origin state.

### 4. Handling data anomalies
Discovered one extreme outlier: CE → AM with 104-day delivery. Investigation confirmed single erroneous order — excluded from final metrics with note in methodology.

## SQL Techniques Used
- INNER/LEFT JOINs across 4+ tables
- Aggregate functions (AVG, COUNT, SUM)
- CASE statements for status categorization
- Window functions (RANK, PERCENTILE_CONT)
- Subqueries and CTEs
- Outlier detection and handling

## Visualization
Delivery Days 

Analysis revealed that 35% of orders arrived before the estimated delivery date, suggesting overestimation of delivery times by sellers in certain regions.
*Chart shows average delay days for routes with >5 orders, outlier excluded.*


## Next Steps (if more time)
- Cohort analysis of customer repeat purchase behavior
- Predict delivery delay using order value and distance
