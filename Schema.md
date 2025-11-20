
## Schema Diagram
CUSTOMERS
---------
customer_id (PK)
name
signup_date
location

ORDERS
---------
order_id (PK)
customer_id (FK → customers.customer_id)
order_date
payment_method

ORDER_ITEMS
---------
order_item_id (PK)
order_id (FK → orders.order_id)
product_id (FK → products.product_id)
quantity
unit_price

PRODUCTS
---------
product_id (PK)
category
cost
price

RETURNS
---------
order_id (FK → orders.order_id)
return_date
reason
