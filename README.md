**Amazon Product Review Analysis**

### 1. **Project Overview**

This Excel-based analysis explores Amazon product review data to uncover insights into product performance, customer satisfaction, pricing strategies, and sales potential. The dataset includes product name, category, actual price, discounted price, rating, rating count, and discount percentage.


### 2. **Data Preparation (Excel)**

* Cleaned and converted price columns from text to numeric.
* Created a column for `Discount (%)`:

```excel
=ROUND((Actual Price - Discounted Price) / Actual Price * 100, 2)
```

* Created a column for `Potential Revenue`:

```excel
=Actual Price * Rating Count
```

* Bucketed `Price Ranges` using formula:

```excel
=IF(Actual Price<200,"<₹200",IF(Actual Price<=500,"₹200–₹500",">₹500"))
```


### 3. **Pivot Table Analysis**

#### a. **Top Performing Products**

* Used pivot table to rank products by:

  * Highest average rating
  * Highest number of reviews
  * Combined score (Rating × Rating Count)

#### b. **Category-Based Analysis**

* Total number of products per category
* Total number of reviews per category
* Average price vs discounted price per category
* Total potential revenue by category

#### c. **Pricing & Discount Insights**

* Number of products with discount ≥ 50%
* Average discount % by category
* Correlation between discount and product rating (observational)

#### d. **Rating Distribution**

* Created a pivot showing count of products per rating (3.0, 4.0, 4.5, etc.)

#### e. **Price Range Buckets**

* Count of unique products per price bucket (<₹200, ₹200–₹500, >₹500)


### 4. **Dashboard Design**

Built a visual dashboard in Excel using:

* Slicers for category and rating range
* Pivot charts: Bar, Column, Pie for:

  * Rating distribution
  * Price range count
  * Top-rated products
* Conditional formatting to highlight high-discount, high-rating items


### 5. **Insights & Recommendations**

* Categories like Electronics and Home Appliances generated the highest revenue.
* Products with discounts of 40–50% received the highest review counts.
* Rating and number of reviews are positively correlated with sales potential.
* Suggest prioritizing products rated ≥ 4.5 for promotions.
* Focus on bundles or upsells for products in ₹200–₹500 range.

### 6. **Next Steps**

* Track time-based review trends (weekly/monthly).
* Add sentiment analysis for written reviews if available.
* Set up Excel Power Query connections for real-time data refresh.


**Prepared by:** \[Your Name]
**Tool:** Microsoft Excel
**Date:** \[Insert Date]
