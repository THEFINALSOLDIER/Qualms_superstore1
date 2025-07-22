# Qualms_superstore

## overview
This is a report analysis of the qualms superstore dataset
+ product category report
+ regional sales report
+ sales
---
> This a point of sales report
## SQL queries
````sql
SELECT * FROM sales_data;
````
````sql
--- Sales channel ---
SELECT sales_channel,COUNT (Sales_Channel) AS count_of_sales FROM Sales_data
group BY Sales_Channel
ORDER BY sales_channel DESC ;
````
````sql
--- Payment method ---
SELECT payment_method,COUNT(payment_method) AS count_of_payment_method FROM Sales_data
GROUP BY Payment_Method 
ORDER BY COUNT(Payment_Method) DESC ;
````
````sql
--- Product category ---
SELECT product_category,SUM (sales_amount) AS count_of_product_category FROM Sales_data
group BY product_category
ORDER BY SUM (sales_amount) DESC ;
````
````sql
--- Total sales ---
SELECT SUM(sales_amount) AS Total_sales 
FROM Sales_data ;
````
````sql
--- Total cost ---
SELECT SUM(unit_cost) AS Total_cost
FROM Sales_data ;
````
````sql
--- Total discount ---
SELECT SUM(discount) AS Total_discount
FROM Sales_data ;
````
````sql
--- Total quantity sold ---
SELECT SUM(quantity_sold) AS Total_quantity_sold
FROM Sales_data ;
````
````sql
--- Total quantity sold by region and sales rep ---
SELECT Region_and_Sales_Rep ,SUM(quantity_sold) AS Total_quantity_sold
FROM Sales_data 
GROUP BY Region_and_Sales_Rep 
ORDER BY SUM(quantity_sold) DESC;
````
### PowerBI visualization

<img width="1318" height="741" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/58faa242-883d-4258-9a9d-3522d14ed074" />

#### PowerBI visuals 

[click here to view](https://ibb.co/69tVjqd)
[click here to view](https://ibb.co/qvzS5W2)
