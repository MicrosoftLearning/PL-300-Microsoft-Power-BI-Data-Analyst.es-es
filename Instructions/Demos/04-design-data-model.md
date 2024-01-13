---
lab:
  "\_\_ title": Design a data model in Power BI
  "\_\_ module": Design a data model in Power BI
---
# Diseño de un modelo de datos en Power BI

## Revisión del modelo

1. En el panel Datos, expanda todas las tablas para revelar los campos.

1. En la tabla Sales, señale la jerarquía OrderDate, que se creó automáticamente.

1. Explique que se creará una tabla de fechas en la próxima demostración.

1. En la vista de modelo, mantenga el cursor sobre la relación creada automáticamente entre las dos tablas.

1. Explique cómo se propagarán los filtros de la tabla Product a la tabla Sales.

## Crear una jerarquía

1. Cree una jerarquía basada en la columna Category de la tabla Product.

1. Cambie el nombre de la jerarquía a Products.

1. Agregue la columna Product como segundo nivel.

## Establecimiento de las propiedades de modelo

1. Oculte ambas columnas de ProductID.

1. Aplíquele formato a la columna Quantity para usar el separador de miles.

1. Realice una selección múltiple de las columnas Sales y Unit Price y aplíqueles formato para usar dos posiciones decimales.

## Validación del diseño del modelo con un objeto visual de matriz

1. En la vista Informe, agregue un objeto visual de matriz a la página y, a continuación, cambie su tamaño para que llene toda la página.

1. Agregue la jerarquía Products a las filas y luego agregue los campos Quantity, Sales y Unit Price.

1. Expanda todos los niveles de la jerarquía Products.

1. Señale que los valores de Unit Price son la suma de los precios, lo cual no es correcto.

1. En el panel Datos, seleccione el campo Precio unitario y configure su resumen para usar Promedio.

1. Elimine la columna Sum of Unit Price del objeto visual de matriz y luego vuelva a agregar el campo Unit Price.

1. Guarde el archivo de Power BI Desktop.

1. Deje el archivo de Power BI Desktop abierto para la próxima demostración.
