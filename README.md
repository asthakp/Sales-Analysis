# Sales Analysis Project
## Overview
This project analyzes 12 months of sales data to answer key business questions and identify trends. The focus is on uncovering high-performing products, sales timing, and customer purchasing behavior. By cleaning and visualizing the data, the analysis provides actionable insights for better decision-making.

## Steps in the Project
### 1. Data Preparation
The project begins by combining and cleaning the data for analysis: 

Merged Monthly Data: Combined 12 months of sales data into a single DataFrame using pd.concat. 

### Data Cleaning:
Dropped NaN values to ensure the dataset was complete. 

Removed invalid rows based on specific conditions. 

Changed column data types for consistency: 

Converted Order Date to datetime format. 

Converted price-related columns to numeric format. 

Column Extraction: Focused on three key columns—Month, Sales, and City. 


### 2. Business Questions and Insights
### What was the best month for sales?
Using groupby on the Month column, we calculated the total sales for each month. 

Visualized the results with a bar chart to show monthly trends. 

Identified the best-performing month and its total earnings. 


### What city sold the most products?
Grouped sales data by city to calculate total sales for each location. 

Displayed city-wise performance using a bar chart. 

### What time should we display advertisements to maximize sales?
Analyzed Order Date to extract the hour of purchase. 

Created a line chart to visualize customer buying behavior over a 24-hour period. 

Determined peak hours for advertisements to maximize customer engagement. 

### What products are most often sold together?
Used the itertools.combinations and collections.Counter libraries to identify product pairs frequently bought together. 

Grouped products by Order ID and split the items in each transaction to generate all possible pairs. 

Output the top 10 most common product combinations. 

### What product sold the most, and why?
Grouped data by Product to calculate total quantity sold and mean price per product. 

Visualized the relationship between product prices and quantities sold using a dual-axis chart: 

A bar chart for the quantity sold. 

A line plot for average prices. 
### Insights:
Lower-priced products sold more due to affordability. 

High-priced items like MacBook Pro and ThinkPad laptops performed decently, possibly due to necessity or customer willingness to invest in quality. 

### 3. Tools and Techniques
### Libraries:
pandas: Data manipulation and cleaning. 

matplotlib: Data visualization.

itertools: For generating product combinations. 

collections.Counter: Counting and ranking frequent pairs. 

### Key Insights
### Best Month for Sales:
December was the top-performing month for sales, likely due to the holiday season when people shop extensively.

January saw a significant drop in sales, possibly because customers completed their shopping during December.

### Top City for Sales:
San Francisco recorded the highest sales, suggesting strong customer engagement and spending habits.

Portland had the lowest sales, which might indicate fewer customers or less demand in that area.

### Optimal Advertisement Timing:
Most purchases occurred during 11 AM-12 PM and 7 PM, highlighting these as prime hours for customer activity.

Advertising campaigns should start at least one hour earlier to capture attention before peak shopping times.

### Frequently Bought Together Products:
The top product combinations were:

iPhone and Lightning Charging Cable (1005 orders)

Google Phone and USB-C Charging Cable (987 orders)

iPhone and Wired Headphones (447 orders)

### Recommendations:
Rearrange physical store layouts so these products are placed next to each other.

In online stores, implement a feature to recommend the second product when the first is added to the basket.

Offer deals or discounts when these products are bought together.

### Top-Selling Products and Pricing Trends:
Cheaper products sold the most, likely due to affordability.

Expensive products like laptops (e.g., MacBook Pro, ThinkPad) performed decently, possibly because they fulfill critical needs (e.g., for students or professionals) or are perceived as high-value items.
