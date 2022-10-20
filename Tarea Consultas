/*Bases-de-Datos-Relacionales
Tarea de Consultas de Bases de Datos Relacionales MCD
Alan Fernando Mejia Aranda*/

SELECT  A.SKU,
		A.L13UnitsTotal,
		B.CATEGORY
FROM Analysis..SKUINFO A
LEFT JOIN APPS..ITEM_CLASSIFICATION B ON A.SKU=B.SKU
WHERE B.[Group]='UNDERCAR' AND A.ITEM_STATUS='A' AND A.L13UnitsTotal>0



SELECT  (SUM (A.L13UnitsTotal)/COUNT (A.L13UnitsTotal)) AS media, -- sacamos la media
		AVG (A.L13UnitsTotal) AS media2, --otra manera de sacar la media
		MIN (A.L13UnitsTotal) AS valor_minimo, -- sacamos el valor minimo
		MAX (A.L13UnitsTotal) AS valor_maximo, -- sacamos el valor maximo
		(COUNT (A.L13UnitsTotal)/2) AS mediana
FROM Analysis..SKUINFO A
LEFT JOIN APPS..ITEM_CLASSIFICATION B ON A.SKU=B.SKU
WHERE B.[Group]='UNDERCAR' AND A.ITEM_STATUS='A' AND A.L13UnitsTotal>0




SELECT  top 1 A.L13UnitsTotal as MODA,
		COUNT(A.L13UnitsTotal) AS Frecuencia --contamos las frecuencias
FROM Analysis..SKUINFO A
	LEFT JOIN APPS..ITEM_CLASSIFICATION B ON A.SKU=B.SKU
WHERE B.[Group]='UNDERCAR' AND A.ITEM_STATUS='A' AND A.L13UnitsTotal>0
GROUP BY A.L13UnitsTotal
ORDER BY COUNT(A.L13UnitsTotal) DESC --agrupamos y ordenamos de mayor frec a menor
