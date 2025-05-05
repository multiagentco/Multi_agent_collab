 ```sql
SELECT 
    SUM(oi.quantity * oi.unit_price) AS total_sales
FROM 
    order_items oi
JOIN 
    orders o ON oi.order_id = o.order_id
WHERE 
    EXTRACT(YEAR FROM o.order_date) = EXTRACT(YEAR FROM CURRENT_DATE) - 1;
``` 