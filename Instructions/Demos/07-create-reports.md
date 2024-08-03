---
demo:
  title: Creación de informes en Power BI
  module: Create reports in Power BI
---
# Crear informes

## Creación de un informe de una sola página

1. Elimine el objeto visual de matriz que se usó para probar y validar los cálculos del modelo.

1. Cambie el nombre de la página del informe a Resumen de ventas.

## Adición de una segmentación

1. Agregue una segmentación para la columna Año de la tabla Fecha y colóquela en la parte superior izquierda de la página del informe.

1. Utilice las opciones de formato para configurar la segmentación para una selección única.

## Adición de varios objetos visuales

1. Agregue un gráfico de líneas y columnas apiladas a la página y configúrelo de la siguiente manera:

    - Eje compartido: Date | Month

    - Valores de columna: Sales | Sales

    - Valores de línea: Sales | Profit Margin

1. Use la segmentación para filtrar la página por CY2019 y luego por CY2020.

1. En el gráfico de líneas y columnas apiladas, indique que no hay una columna de ventas para diciembre de 2020.

1. Configure el eje compartido para "mostrar elementos sin datos".

1. Señale que se agrega diciembre de 2020 al eje, pero no hay columna de datos.

1. Explique que los datos de ventas de diciembre de 2020 aún no han sucedido. *Ejecutarás un script en una demostración posterior para cargar las ventas de diciembre de 2020.*

1. Agregue un gráfico de embudo y configúrelo de la siguiente manera:

    - Grupo: Product | Category

    - Valores: Sales | Profit Margin

1. Utilice las opciones de formato para seleccionar un color de datos que contraste.

1. Agregue un objeto visual de Preguntas y respuestas y escriba la siguiente pregunta: Ventas totales por producto demográfico

1. Guarde el archivo de Power BI Desktop.

1. Deje el archivo de Power BI Desktop abierto para una demostración posterior.
