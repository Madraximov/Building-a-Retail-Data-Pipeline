![Walmart E-Commerce](walmartecomm.jpg)

# Walmart E-Commerce Sales Analysis Project

Walmart is the biggest retail store in the United States. Just like others, they have been expanding their e-commerce part of the business. By the end of 2022, e-commerce represented a roaring $80 billion in sales, which is 13% of total sales of Walmart. One of the main factors that affects their sales is public holidays, like the Super Bowl, Labour Day, Thanksgiving, and Christmas.

In this project, you have been tasked with creating a data pipeline for the analysis of supply and demand around the holidays, along with conducting a preliminary analysis of the data. You will be working with two data sources: grocery sales and complementary data. You have been provided with the `grocery_sales` table in a `PostgreSQL` database with the following features:

## `grocery_sales` Table
- `index`: unique ID of the row
- `Store_ID`: the store number
- `Date`: the week of sales
- `Weekly_Sales`: sales for the given store

Also, you have the `extra_data.parquet` file that contains complementary data:

## `extra_data.parquet`
- `IsHoliday`: Whether the week contains a public holiday - 1 if yes, 0 if no.
- `Temperature`: Temperature on the day of sale
- `Fuel_Price`: Cost of fuel in the region
- `CPI`: Prevailing consumer price index
- `Unemployment`: The prevailing unemployment rate
- `MarkDown1`, `MarkDown2`, `MarkDown3`, `MarkDown4`: Number of promotional markdowns
- `Dept`: Department number in each store
- `Size`: Size of the store
- `Type`: Type of the store (depends on `Size` column)

## Objective
I worked to merge these files and perform some data manipulations. The transformed DataFrame can then be stored as the `clean_data` variable containing the following columns:
- `Store_ID`
- `Month`
- `Dept`
- `IsHoliday`
- `Weekly_Sales`
- `CPI`
- `Unemployment`

After merging and cleaning the data, you will have to analyze the monthly sales of Walmart and store the results of your analysis as the `agg_data` variable that should look like:

| Month | Weekly_Sales     |
|-------|------------------|
| 1.0   | 33174.178494     |
| 2.0   | 34333.326579     |
| ...   | ...              |

Finally, you should save the `clean_data` and `agg_data` as CSV files.

It is recommended to use `pandas` for this project.

