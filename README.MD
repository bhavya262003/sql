# E-Commerce Project

### Objective:
1.	Explore the structure of the dataset by understanding the relationships between tables.
2.	Formulate SQL queries to extract meaningful insights from the data.

```
select * from list_of_orders
```

 ![alt text](image-3.png)

```
select * from order_details
```
![alt text](image-4.png)

```
select * from sales_target
```

![alt text](image-5.png)

#### Analysis
1. Order_id is common in list_of_orders and order_details
2. Category is common in order_details and sales_target

#### Basic Queries:
1. Count of rows in each table

```
SELECT 'list_of_orders' AS Table_Name, COUNT(*) AS RowCount FROM list_of_orders
UNION
SELECT 'order_details' AS order_details, COUNT(*) AS RowCount FROM order_details
UNION
SELECT 'sales_target' AS sales_target, COUNT(*) AS RowCount FROM sales_target;
```
![alt text](image-6.png)

#### Customer Analysis:
•	Find the total number of customers.
```
Select distinct count(customername) as Total_no_of_customers from list_of_orders
```
![alt text](image-7.png)

•	Identify the top 5 states with the highest number of customers.
```
select state, count(customername) as no_of_customers from list_of_orders
group by state
order by no_of_customers desc
limit 5
```
![alt text](image-8.png)


• Calculate the average order value for each customer.

![alt text](image-9.png)
=======
```
