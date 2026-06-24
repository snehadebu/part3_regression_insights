# Regression-Based Business Insights & Model Interpretation

## Business Problem Summary

The leadership team of a retail chain wants to understand which factors are most strongly associated with monthly sales performance across stores. The objective is to identify business drivers that can support decisions related to marketing investment, inventory management, staffing, and store operations.

---

## Dataset Description

The dataset contains store-level monthly operational and sales information, including:

* Store ID
* Month
* Region
* Store Type
* Marketing Spend
* Footfall
* Average Discount Percentage
* Staff Count
* Inventory Availability Percentage
* Competitor Distance
* Holiday Flag
* Customer Rating
* Monthly Sales
* Monthly Profit

---

## Dependent Variable

**monthly_sales**

This variable was selected as the target variable because the business objective is to understand factors associated with sales performance.

---

## Independent Variables

The following variables were considered as potential predictors:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* customer_rating

Categorical variables:

* region
* store_type
* holiday_flag

---

## Dummy Variable Approach

The categorical variable **region** was converted into dummy variables.

Reference Category:

**East**

Dummy Variable Used:

**region_north**

The reference category was excluded to avoid dummy variable redundancy.

---

## Regression Approach

Two simple regression models were created:

### Model 1

Dependent Variable:

* monthly_sales

Independent Variable:

* marketing_spend

Results:

* R² = 0.167

### Model 2

Dependent Variable:

* monthly_sales

Independent Variable:

* footfall

Results:

* R² = 0.736

A multiple regression framework was then developed using:

* footfall
* marketing_spend
* inventory_availability_pct
* region_north

---

## Model Comparison Summary

| Model           | R²    |
| --------------- | ----- |
| Marketing Spend | 0.167 |
| Footfall        | 0.736 |

Footfall demonstrated substantially stronger explanatory power than marketing spend.

---

## Final Model Selected

Multiple Regression Model

Variables Included:

* footfall
* marketing_spend
* inventory_availability_pct
* region_north

Reason for Selection:

The model incorporates multiple operational and business drivers simultaneously and provides a more comprehensive understanding of sales performance.

---

## Business Recommendation

Based on the analysis:

1. Prioritize initiatives that increase customer footfall.
2. Maintain strong inventory availability levels.
3. Continue targeted marketing investments.
4. Monitor regional performance differences.
5. Use regression insights to support resource allocation decisions.

---

## Assumptions and Limitations

* Regression identifies association rather than causation.
* External factors affecting sales may not be included in the dataset.
* Regional differences may reflect local market conditions not captured by the model.
* Additional variables may improve predictive performance.

---

## Screenshots Included

* simple_regression_output.png
* multiple_regression_output.png
* residuals_preview.png
* model_comparison_preview.png
