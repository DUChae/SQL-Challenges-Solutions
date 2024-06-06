SELECT Customers.name AS Customers <br/>

FROM Customers <br/>

LEFT JOIN Orders ON Customers.id=Orders.customerId <br/>

WHERE CustomerId IS NULL