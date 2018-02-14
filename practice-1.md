# SQL statements practice run with SQL Tryit Editor
- https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_or

1. SELECT * FROM customers;
2. SELECT * FROM orders;
3. SELECT * FROM products ORDER BY Price DESC;
4. SELECT customerName, 
COUNT (*) AS 'number of orders'
    FROM customers 
    INNER JOIN orders 
    ON orders.customerID = customers.customerID
    GROUP BY customers.customerID;
5. SELECT 
    username,
    photos.id,
    photos.image_url, 
    COUNT(*) AS total
FROM photos
INNER JOIN likes
    ON likes.photo_id = photos.id
INNER JOIN users
    ON photos.user_id = users.id
GROUP BY photos.id
ORDER BY total DESC
LIMIT 1;