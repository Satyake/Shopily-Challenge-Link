# Shopily-Challenge-Link
Repo for Spotify challenge


**Solutions for the SQL challenges:

Answer 1

****SELECT count(orderid) from orders join shippers on orders.shipperid=shippers.shipperid where shippername='Speedy Express';
**54 orders


Answer 2

SELECT lastname,count(orders.orderid) FROM employees join orders on employees.employeeid=orders.employeeid group by lastname order by count(orders.orderid) desc;

**Peacock**

Answer 3


**create view newtable as
select orders.orderid, customers.country, orderdetails.quantity, products.productname
from orders, orderdetails
join customers ON orders.customerid=customers.customerid
join products ON orderdetails.productid=products.productid
where country='Germany';


**create view product_orders AS
select productName, quantity, COUNT(*) as 'Orders'
from products_ordered
group by  productname;**


**select orders*quantity,productname from product_orders order by orders*quantity desc;


SELECT * FROM newtable where country='Germany' and productname ='Camembert Pierrot';
****

Camembert Pierrot was ordered most amount in germany.

