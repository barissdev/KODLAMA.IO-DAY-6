# KODLAMA.IO-DAY-6


SELECT 
    P.ProductName AS 'Ürün Adı', 
    SUM(OD.UnitPrice * OD.Quantity) AS 'Kazanılan Toplam'
FROM 
    OrderDetails OD
INNER JOIN 
    Products P ON OD.ProductID = P.ProductID
INNER JOIN 
    Orders O ON OD.OrderID = O.OrderID
GROUP BY 
    P.ProductName;
