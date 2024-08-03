---
demo:
  title: "Limpieza, transformación y carga de datos en Power\_BI"
  module: 'Clean, transform, and load data in Power BI'
---

# Limpieza, transformación y carga de datos en Power BI

## Aplicación de transformaciones de consulta

1. Primero, aplique transformaciones a la consulta Product.

1. Elimine las columnas RetailPrice, Photo y Sales.

1. Cambie el tipo de datos de la columna Canales a Número entero.

1. Cambiar el nombre de las columnas siguientes:

    - ProductSKU a SKU

    - ProductName a Product

    - ProductCategory a Category

    - ItemGroup a Item Group

    - KitType a Kit Type

1. En segundo lugar, aplique transformaciones a la consulta Sales.

1. Elimine todas las columnas, excepto las siguientes:

    - OrderDate

    - ProductID

    - Cantidad

    - UnitPrice

1. Cambie el tipo de datos de la columna UnitPrice a Número decimal fijo.

1. Cambie el nombre de la columna UnitPrice a Precio unitario.

1. Realice una selección múltiple de las columnas Cantidad y Unit Price y, a continuación, agregue una nueva columna en función de su multiplicación.

1. Cambie el nombre de la nueva columna a Sales.

## Integración de consultas

1. Cree una consulta mediante el conector de Excel, conectándose al archivo D:\Allfiles\Demo\Data\ProductCost.xlsx.

1. Elimine la columna Product.

1. Cambie el tipo de datos de la columna ProductCost a Número decimal fijo.

1. Seleccione la consulta Product y luego combínela con la consulta ProductCost, relacionando las columnas SKU.

1. En la ventana Niveles de privacidad, establece el nivel de privacidad de D:\ en Organizativo.

1. Expanda la columna ProductCost para incluir la columna ProductCost (de la consulta ProductCost).

1. Cambie el nombre de la nueva columna a Cost.

## Deshabilitar y cargar consultas en el modelo de datos

1. En el panel Consultas, deshabilite la consulta ProductCost.

1. En la pestaña de la cinta Inicio, haz clic en el icono Cerrar y aplicar.

1. En Power BI Desktop, señale las dos tablas en el panel Datos.

1. Guarde el archivo de Power BI Desktop.

1. Deje el archivo de Power BI Desktop abierto para la próxima demostración.
