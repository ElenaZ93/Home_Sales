# Home_Sales

# Home Sales Analysis with PySpark

In this challenge, you'll use your knowledge of **SparkSQL** to determine key metrics about home sales data. Then you'll use **Spark** to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Project Overview

The goal of this project is to analyze home sales data to determine insights on pricing metrics based on various property attributes. Using SparkSQL, we will:
1. Query average prices based on property characteristics, such as the number of bedrooms and bathrooms.
2. Cache and uncache tables to compare query performance.
3. Partition data by `date_built` and analyze the effects on runtime.
4. Perform runtime comparisons for cached, uncached, and partitioned data.

## Before You Begin

1. **Create Repository**: Start by creating a new repository named `Home_Sales` on GitHub. **Do not add this homework to an existing repository**.
2. **Clone Repository**: Clone the new repository to your computer.
3. **Push Changes**: After completing each step, push your changes to GitHub.

## Files

Download the following files from the resources folder to help you get started:
- **Home_Sales_starter_code.ipynb**: Starter code for the project. Rename this file to **Home_Sales.ipynb** before starting.
- **home_sales_revised.csv**: The dataset containing home sales data, which will be loaded into a Spark DataFrame.

## Instructions

### Setup
1. Rename `Home_Sales_starter_code.ipynb` to `Home_Sales.ipynb`.
2. Import the necessary PySpark SQL functions for this assignment.

### Data Loading
1. Read the `home_sales_revised.csv` data in the starter code into a Spark DataFrame.
2. Create a temporary table called `home_sales`.

### Data Analysis Using SparkSQL

Answer the following questions using SparkSQL:

1. **Average Price of Four-Bedroom Houses by Year**: 
   - What is the average price for a four-bedroom house sold for each year? **Round off your answer to two decimal places**.

2. **Average Price of Three-Bedroom, Three-Bathroom Houses by Year Built**: 
   - What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? **Round off your answer to two decimal places**.

3. **Average Price of Larger Homes by Year Built**: 
   - What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? **Round off your answer to two decimal places**.

4. **Average Price per "View" Rating**:
   - Calculate the average price of a home per "view" rating for homes with an average price greater than or equal to $350,000. **Determine the runtime for this query** and **round off your answer to two decimal places**.

### Caching and Performance Optimization
1. **Cache the Temporary Table:** Cache your home_sales temporary table.

2. Caching temporarily stores data in memory, allowing Spark to access frequently queried data faster than if it had to reload it from disk each time. This technique reduces runtime for repeated queries, especially with large datasets, as it eliminates the need to retrieve data from storage. In this project, caching is used to improve query performance, providing a noticeable difference in runtime between cached and uncached data.

3. **Check Caching:** Verify if the home_sales temporary table is cached.

4. **Run Cached Query:** Using the cached data, re-run the query that calculates the average price of a home per "view" rating for properties with an average home price greater than or equal to $350,000. Determine the runtime and compare it to the uncached runtime.

### Partitioning Data and Additional Query

1. **Partition the Data**: Partition by the `date_built` field on the formatted parquet home sales data.
2. **Create Temporary Table**: Create a temporary table for the parquet data.
3. **Run Query on Partitioned Data**: Re-run the query on partitioned data that calculates the average price of a home per "view" rating for homes with an average price greater than or equal to $350,000. **Determine the runtime** and **compare it to the uncached runtime**.

### Clean-Up

1. **Uncache the Table**: Uncache the `home_sales` temporary table.
2. **Verify Uncaching**: Verify that the `home_sales` temporary table is uncached using PySpark.

### Push to GitHub

1. Download your completed `Home_Sales.ipynb` file.
2. Upload it into your `Home_Sales` GitHub repository.

## Support and Resources

Your instructional team will provide support during classes and office hours. You will also have access to learning assistants and tutors to help you with topics as needed. Make sure to take advantage of these resources as you collaborate with your partner on this project.

Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.
