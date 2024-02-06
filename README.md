# CODIGOS-POWER-BI
Contiene todas las consultas SQL de los POWER BI


SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN SANTA CRUZ' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 002 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END

UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN LA PAZ' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 101 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END
UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN TIENDA CM' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 200 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END

UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN TIENDA CR' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 201 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END

UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN DE IMPORTACIONES' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 001 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END
UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN IT' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 203 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END
UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN DE PRODUCTOS OBERVADOS' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 102 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END
UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN PRODUCTO CONTEO' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 300 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END
UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN MATERIAL EMBALAJE' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 301 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END
UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN TRANSITORIO' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 302 AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END

UNION ALL

SELECT
    FORMAT(T3.[DocDate], 'yyyy-MM') AS 'Mes',
    SUM(T3.[TransValue]) AS 'Valor de la transaccion',
    SUM(T3.[InQty] - T3.[OutQty]) AS 'Cantidad Neta',
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END AS 'COLUMNA',
    'ALMACEN COÑA COÑA' AS 'ALMACEN'
FROM
    OITM T0
INNER JOIN
    OMRC T1 ON T0.[FirmCode] = T1.[FirmCode]
INNER JOIN
    OITB T2 ON T0.[ItmsGrpCod] = T2.[ItmsGrpCod]
INNER JOIN
    OINM T3 ON T0.[ItemCode] = T3.[ItemCode]
WHERE
    T3.Warehouse = 100 OR T3.Warehouse = 304 
AND
    T3.DocDate >= '20230101' 
GROUP BY
    FORMAT(T3.[DocDate], 'yyyy-MM'),
    T0.[ItemName],
    T0.[ItemCode],
    T1.[FirmName],
    T2.[ItmsGrpNam],
    CASE WHEN T0.[ItemCode] IS NOT NULL THEN 'INVENTARIO' ELSE NULL END;
