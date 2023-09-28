## Sales Insights Data Analysis Project 

### Instructions to setup mysql on your local computer
SQL database dump is in sales_stores.sql file above. Download `sales_stores.sql` file to your local computer and import it.

### Data Analysis Using SQL
1. Show all superstore sales dataset records
   
       SELECT * FROM super_stores.'superstore sales dataset'; 

 2. Show total number of superstore sales

        SELECT count(*) FROM 'superstore sales dataset';

3. Show Total Sales by Category
   
       SELECT Category, SUM(Sales) AS TotalSales FROM Sales_report GROUP BY Category;
 
4. Show Top 10 Customers by Profit

        SELECT CustomerName, SUM(Profit) AS TotalProfit FROM Sales_report 
        GROUP BY CustomerName ORDER BY TotalProfit DESC LIMIT 10;
 
5. Show Monthly Sales Trend

        SELECT  SUBSTR(OrderDate, 1, 2) AS Month, SUM(Sales) AS MonthlySales FROM Sales_report 
        WHERE SUBSTR(OrderDate, 7, 2) = '19' GROUP BY Month ORDER BY Month;

6. Show Best-Selling Products

        SELECT ProductName, SUM(Quantity) AS TotalQuantitySold FROM Sales_report 
        GROUP BY ProductName ORDER BY TotalQuantitySold DESC LIMIT 10;

7. Show Profit Margin Analysis
 
        SELECT ProductName, (SUM(Profit) / SUM(Sales)) AS ProfitMargin 
        FROM Sales_report GROUP BY ProductName ORDER BY ProfitMargin DESC;

8. Show Returns Analysis

        SELECT Returns, COUNT(Returns) AS ReturnCount, 
        SUM(Profit) AS TotalProfitLoss FROM Sales_reportGROUP BY Returns;

9. Show Geographical Sales Breakdown

        SELECT Region, SUM(Sales) AS TotalSales 
        FROM Sales_report GROUP BY Region;

10. Show Sales by Payment Mode

         SELECT PaymentMode, SUM(Sales) AS TotalSales 
         FROM Sales_report GROUP BY PaymentMode;

11. Show Customer Segment Analysis

         SELECT Segment, SUM(Sales) AS TotalSales FROM Sales_report GROUP BY Segment;

12. Show Products with Low Stock

         SELECT ProductName, SUM(Quantity) AS TotalQuantity
         FROM Sales_report
         GROUP BY ProductName
         HAVING TotalQuantity < 10;
         

Data Analysis Using Power BI
============================

Access the sales dashboard of our hardware company via the following link: [Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNjA5YTFmYzktZTU3Ni00OGM2LThhMGUtODcwYzcxZjZhY2Y0IiwidCI6IjM0ODJlZWIwLWQ4MzUtNGE5Ni1iZmJhLTQ0NWE3NTExZTE0MSJ9)
