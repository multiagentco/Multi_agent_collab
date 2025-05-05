 To find the top 5 customers, we need to analyze the data in the `customers` and `orders` tables. We will write a SQL query that calculates the total amount spent by each customer and then ranks them to find the top 5.

```sql
SELECT c.customer_id, c.name, SUM(oi.quantity * oi.unit_price) AS total_spent
FROM customers c
JOIN orders o ON c.customer_id = o.customer_id
JOIN order_items oi ON o.order_id = oi.order_id
GROUP BY c.customer_id, c.name
ORDER BY total_spent DESC
LIMIT 5;
``` 