# Home_Sales

In this challenge I use SparkSQL to determine key metrics about home sales data. Also I use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached by performing following steps :

- Import the necessary PySpark SQL functions
- Read the home_sales_revised_csv and create a temporary table to answer foll questions using SparkSQL :
  1. What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
  ![image](https://github.com/Swetavirani/Home_Sales/assets/102982635/1c38ef04-da16-447c-a10f-156fa4b80a85)

  2. What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
  ![image](https://github.com/Swetavirani/Home_Sales/assets/102982635/c252ea34-ac4e-452f-a94e-b130deedca0b)

  3. What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
  ![image](https://github.com/Swetavirani/Home_Sales/assets/102982635/aff34be6-d254-4146-a311-c19d577c57b7)

  4. What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.
  ![image](https://github.com/Swetavirani/Home_Sales/assets/102982635/9226efab-1120-4d89-8f03-e92604c236c0)

  - Cache the tempary table and checked if it was cached
  - Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
  ![image](https://github.com/Swetavirani/Home_Sales/assets/102982635/1f97094d-f9cb-4e22-a72f-99579df53fff)
  - Partition by the "date_built" field on the formatted parquet home sales data.
  - Create a temporary table for the parquet data.
  - Run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
   ![image](https://github.com/Swetavirani/Home_Sales/assets/102982635/18d1d80c-6102-4cad-ae08-923f4d659183)
  
    
      Runtime is 0.32591 seconds with caching as against 0.71490 seconds pre-caching
   - Uncache the home_sales temporary table.
   - Verify that the home_sales temporary table is uncached using PySpark.

