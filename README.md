![Logo](https://user-images.githubusercontent.com/43790576/198089519-336bd6d8-944a-4868-9c26-d07599203949.JPG)
# AdventureWorks-Multiple-Linear-Regression-con-Python

Desarrollo de un modelo de Regresion Lineal Multiple para la base de datos de muestra Adventure Works 2019. Esta corporacion vende bicicletas, por lo que para este caso se ha creado una consulta SQL para obtener la lista de caracteristicas y precio de los productos. Se elaboro el siguiente query en SQL:

    SELECT pp.ProductID, pp.Name, pp.Color, pp.ListPrice AS Price, pp.Size, pp.Weight, pp.DaysToManufacture, pp.SellStartDate, sg.Name as Categoria,

    CASE WHEN pp.Style = 'W' THEN 'Women' WHEN pp.Style = 'M' THEN 'Men' ELSE 'Universal' END AS Estilo

    FROM [Production].[Product] AS pp

    JOIN [Production].[ProductSubcategory] AS sg ON pp.[ProductSubcategoryID] = sg.ProductSubcategoryID

    WHERE pp.Weight IS NOT NULL AND pp.Size IS NOT NULL


El proposito de este notebook es practicar la RLM en Python. Por lo tanto se desea conocer de que manera las caracteristicas de los productos pueden ayudarnos a predecir el precio de las bicicletas que vende Adventure Works. La base se puede descargar en el siguiente link: [AdventureWorks sample databases](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms)

