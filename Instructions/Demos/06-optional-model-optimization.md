---
lab:
  "\_\_ title": (Optional) Optimize model performance in Power BI
  "\_\_ module": Optimize model performance in Power BI
---

# (Opcional) Optimización del rendimiento del modelo

## Revisión de un diseño de modelo de DirectQuery

> **Nota:** Esta demostración usa un archivo diferente de Power BI Desktop.

1. Abra el archivo D:\PL300\Demo\Resources\AW Sales Analysis.pbix.

1. Si se le solicita que se conecte al origen de datos, haga clic en Conectar.

1. En la esquina inferior derecha, señale que el modelo de datos comprende tablas de DirectQuery.

1. Guarde el archivo de Power BI Desktop en la carpeta D:\PL300\Demo\MySolution.

1. En la vista Modelo, introduzca el diseño del modelo, que incluye dos tablas relacionadas.

1. En la vista Informe, interactúe con el informe seleccionando diferentes elementos en la segmentación Fiscal Year.

1. Obtenga detalles de cualquier columna de mes para revelar los detalles del pedido.

1. Vuelva a la página Resumen de ventas.

## Revisión del rendimiento de consultas

1. En la pestaña de la cinta Ver, muestre el panel Analizador de rendimiento.

1. Actualice los objetos visuales y, a continuación, expanda la segmentación y el objeto visual Sales by Month.

1. Indique que se ha usado el modo DirectQuery (los datos se han solicitado del origen de datos).

## Configuración de tablas de almacenamiento Dual

1. En la vista Modelo, seleccione la tabla Date y luego seleccione el modo de almacenamiento en Dual.

1. Cuando los datos se hayan importado, cambie a la vista Informe y, después, en el panel Analizador de rendimiento, actualice los objetos visuales.

1. Señale que la tabla Fecha ahora se consulta desde la memoria caché del modelo.

## Creación de agregaciones

1. Abra la ventana del Editor de Power Query y, en el panel Consultas, duplique la consulta Ventas del distribuidor.

1. Cambie el nombre de la nueva consulta a Agregación de ventas del distribuidor.

1. Aplique un grupo por transformación de la siguiente manera:

    - Agrupe por OrderDate.

    - Nueva columna: Sales, que es la suma de la columna SalesAmount.

1. Cierre y aplique las consultas.

1. En la vista Modelo, configure el modo de almacenamiento para la tabla Reseller Sales Agg en Importar.

1. Cree una relación desde la columna Fecha de la tabla Fecha hasta la columna OrderDate de la tabla Agregación de ventas del distribuidor. Asegúrese de que la columna tenga una cardinalidad de uno a varios, con la tabla Fecha en el lado de uno.

1. Administre agregaciones en la tabla Agregación de ventas del distribuidor:

    - OrderDate: agrupe por la columna OrderDate de la tabla Ventas del distribuidor.

    - Sales: sume la columna SalesAmount de la tabla Ventas del distribuidor.

1. Señale que la tabla de agregación ahora está oculta.

1. Cambie a la vista Informe y, después, en el panel Analizador de rendimiento, actualice los objetos visuales.

1. Señale que la tabla Sales by Month ahora se consulta desde la memoria caché del modelo.

1. Obtenga detalles de cualquier mes y señale que los detalles de la tabla se solicitan como DirectQuery desde el origen de datos.

1. Guarde el archivo de Power BI Desktop.

1. Cierre Power BI Desktop.

> **Nota:** No volverá a usar esta solución de Power BI Desktop.
