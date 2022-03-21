- 👋 Hi, I’m @kelintn
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

/* Consultas correlacionadas analizarla consulta las ordenes que contienen el producto 23 y que su cantidad fue a 20 */


Select  o.customerid, o.orderid, o.orderdate from orders as o
  where
    (select d.Quantity from [Order Details] as d 
      where d.ProductID = 23 and o.orderID=d.OrderID ) > 20

