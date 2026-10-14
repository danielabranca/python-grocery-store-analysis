# Instacart Grocery Basket Analysis

## Project Overview

Instacart is an online grocery platform that connects customers with the products they need. Although the company already generates strong sales, understanding when customers order, what they purchase, and how their habits differ can help improve marketing and sales strategies.

This project explores Instacart's grocery shopping data to identify purchasing patterns, examine customer loyalty, and develop customer profiles that could support more targeted marketing campaigns.

The analysis was developed using Python and exploratory data analysis to translate raw data into business-relevant insights.

## Business Questions

The analysis focuses on the following questions:

- **Ordering patterns:** When are customers most and least likely to place orders?
- **Spending behaviour:** How does product price vary throughout the day, and which customer groups demonstrate different spending patterns?
- **Product popularity:** Which product departments account for the highest frequency of orders?
- **Customer loyalty:** How are customers distributed across loyalty groups, and how does ordering behaviour differ between them?
- **Customer segmentation:** How do demographic characteristics, family situation, and shopping habits help distinguish customer groups?
- **Regional differences:** Do customer profiles and purchasing patterns vary across US regions?

The intended audience includes Instacart's marketing and sales leadership, with the ultimate goal of supporting more relevant promotions, product recommendations, and customer engagement strategies.

## Key Insights

### 1. Ordering Activity Varies Throughout the Day

The distribution of orders shows that activity is concentrated during the daytime. In the analysed subset, the busiest hours appear to be around **10 a.m. and 11 a.m.**, followed by the early to mid-afternoon. Activity is considerably lower during the early morning hours.

This pattern could help the marketing team explore when to schedule promotional campaigns, while considering the distinction between periods of high order volume and periods when additional incentives might encourage demand.

![Distribution of orders by hour of day](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/04%20Analysis/Visualizations/hist_order_hour_of_day.png)

*Figure 1. Distribution of orders across the 24-hour day.*

### 2. Product Departments Offer Opportunities for Targeted Promotions

The exploratory analysis identifies **Produce, Dairy and Eggs, Beverages, Snacks, Frozen, and Pantry** among the departments with the highest order frequency.

These departments may provide useful starting points for campaigns designed around frequently purchased grocery categories. Further analysis would be needed to distinguish high order frequency from revenue, profit margin, and growth potential.

![Customer profiles versus departments](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/04%20Analysis/Visualizations/customer_profiles_vs_departments_named.png)

*Figure 2. Distribution of product departments across the customer profiles defined in this project.*

### 3. Customer Profiles Reveal Different Shopping Patterns

The analysis explores customer segments using demographic and behavioural variables, including age, income, number of dependants, product department, and order timing.

The resulting categories include Young Single, Young Parent, Family Shopper, Budget Shopper, Senior Saver, and Affluent Retiree. Additional behavioural categories, such as Late-night Shopper and Weekend Shopper, are also explored.

These profiles provide a starting point for investigating how customer groups differ in their product preferences and ordering behaviour. They should be treated as exploratory segments rather than established customer personas until their definitions and underlying counts have been validated.

![Distribution of customer profiles](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/04%20Analysis/Visualizations/4.10.customer_profiles_distribution.png)

*Figure 3. Distribution of the customer profiles created during the exploratory analysis.*

![Customer profiles across regions](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/04%20Analysis/Visualizations/4.10.customer_profiles_across_regions.png)

*Figure 4. Customer profile distribution across US regions.*

### 4. Demographic Characteristics Provide Context for Segmentation

The analysis also examines relationships between age, income, and number of dependants.

The age-versus-dependants visualisation does not show a clear overall trend in the analysed data. The age-versus-income scatterplot, meanwhile, helps explore how income is distributed across different age groups.

These relationships can inform further segmentation work, but demographic variables alone should not be assumed to explain purchasing behaviour. Their usefulness depends on whether they reveal meaningful differences in order frequency, product choices, or spending.

![Age and family size](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/04%20Analysis/Visualizations/age_and_family_size.png)

*Figure 5. Relationship between customer age and number of dependants.*

![Age and spending power](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/04%20Analysis/Visualizations/age_and_spending_power.png)

*Figure 6. Distribution of income across customer ages.*

## Recommendations

Based on the exploratory findings, the following opportunities merit further investigation:

1. **Test campaign timing.** Use observed ordering patterns to test whether promotions perform better during quieter periods or around established shopping peaks. Measure conversion and incremental orders rather than relying on order volume alone.

2. **Explore department-specific promotions.** Investigate frequently ordered departments such as Produce, Dairy and Eggs, and Beverages to identify suitable products for cross-selling, bundles, and personalised recommendations.

3. **Validate customer segments.** Review the profile definitions and test whether the resulting groups differ consistently in order frequency, average product price, and department preferences.

4. **Investigate regional variation.** Compare customer behaviour across regions to determine whether localised promotions or product recommendations could improve engagement.

5. **Measure campaign performance.** Treat these findings as hypotheses for testing. Compare campaign outcomes against a baseline or control group before concluding that a particular targeting strategy increases sales.

## Data and Methodology

The project combines Instacart grocery-shopping data with a customer dataset supplied for the CareerFoundry exercise. The analysis uses Python notebooks to prepare the data, investigate its quality, combine datasets, derive variables, aggregate results, and create visualisations.

The project covers the following stages:

| Stage | Purpose |
|---|---|
| **Data Wrangling** | Prepare datasets and standardise variables for analysis. |
| **Consistency Checks** | Investigate data types, missing values, duplicates, and data quality issues. |
| **Combining and Extracting Data** | Merge relevant datasets and create analysis-ready subsets. |
| **Deriving Variables** | Create new variables and flags for loyalty, customer activity, and customer profiling. |
| **Grouping and Aggregating** | Summarise ordering behaviour and compare customer groups. |
| **Data Visualisation** | Use charts to explore order timing, customer demographics, loyalty, regional differences, and product departments. |

### Tools and Libraries

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Polars

## Repository Structure

The repository contains notebooks covering the different stages of the analysis, from initial data preparation to customer profiling and visualisation.

- **Data Wrangling:** initial preparation and exploration of the source datasets. You can find it [here.](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/03%20Scripts/4.4%20Data%20Wrangling-Task%20submission.ipynb)
- **Consistency Checks:** investigation and treatment of data quality issues. You can find it [here.](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/03%20Scripts/4.5%20Data%20Consistency%20Checks_task_submission.ipynb)
- **Combining and Extracting Data:** merging datasets and exporting subsets. You can find it [here.](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/03%20Scripts/4.6%20Combining%20and%20Extracting%20Data.ipynb)
- **Deriving Variables:** creating analytical variables and customer classifications. You can find it [here.](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/03%20Scripts/4.7%20Deriving%20Variables-Final%20Version.ipynb)
- **Grouping and Aggregating:** summarising behaviour across customer groups. You can find it [here.](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/03%20Scripts/4.8%20Grouping%20and%20Aggregating.ipynb)
- **Data Visualisation:** exploring order patterns, loyalty, demographics, and customer profiles. You can find it [here.](https://github.com/danielabranca/python-grocery-store-analysis/blob/main/03%20Scripts/4.10.%20Data%20Viz%20-%20Kaggle.ipynb)

The notebooks document the analytical process and provide the code behind the findings presented in this README.

## Limitations and Considerations

- **Sampling:** Some visualisations use a random subset of the data because the full dataset is large and memory resources are limited. Results from a subset should not automatically be treated as exact full-dataset totals.
- **Customer counts:** The later profiling analysis works with merged order-product-customer records. Counts of these records do not necessarily represent counts of unique customers.
- **Profile definitions:** Demographic profiles and behavioural labels are combined in the exploratory workflow. A customer's profile can be overwritten by later rules, so the categories require refinement before they are used for business decisions.
- **Spending measures:** Product prices, average product prices, and total order expenditure are different measures. They should be clearly distinguished when interpreting the charts.
- **Data privacy:** Customer information should be handled responsibly. Direct identifiers, such as first and last names, should not be included in published analytical outputs.
- **Correlation and causation:** The analysis explores patterns and associations. It does not establish that a particular customer characteristic causes a purchasing behaviour or that a proposed campaign will increase sales.

These limitations should be addressed before using the exploratory results to make operational decisions.

## Data Sources

- **Instacart:** *The Instacart Online Grocery Shopping Dataset 2017*. Accessed via Kaggle on October 13, 2026.
- **Customer dataset:** Customer information supplied as part of the CareerFoundry Data Analytics project.

The project brief and customer dataset form part of the CareerFoundry exercise; the brief notes that this customer dataset was created for the project.

## Project Outcome

This project demonstrates an end-to-end exploratory data analysis workflow, from data preparation and quality checks to feature engineering, aggregation, visualisation, and business-oriented interpretation.

It also highlights the importance of validating customer segments and analytical assumptions before translating patterns in the data into targeted marketing strategies.
