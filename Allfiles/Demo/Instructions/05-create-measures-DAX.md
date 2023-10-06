---
demo:
  "\_\_ title": Create measures using DAX in Power BI
  "\_\_ module": Create measures using DAX in Power BI
---
# Creación de medidas mediante DAX en Power BI

> **Sugerencia**: Todos los cálculos se pueden copiar desde el archivo D:\PL300\Demo\Resources\Snippets-Demo-05.txt.

## Creación de una tabla calculada

1. Cree una tabla calculada usando la siguiente expresión:

```dax
Date = CALENDARAUTO()
```

1. Cambie a la vista de datos y revise la tabla, que consta de una sola columna de fecha.

Crear columnas calculadas

1. Agregue una columna calculada a la tabla Date:

```dax
Year = "CY" & YEAR('Date'[Date])
```

1. Agregue una columna calculada adicional a la tabla Date:

```dax
Month = FORMAT('Date'[Date], "YYYY-MM")
```

1. En la vista Modelo, cree una relación arrastrando la columna Fecha de la tabla Fecha a la columna OrderDate de la tabla Ventas.

1. Oculte la columna OrderDate de la tabla Ventas.

1. En la tabla Date, cree la jerarquía Calendar, con los niveles Year y Month.

1. En la vista Informe, marque la tabla Date como una tabla de fechas mediante la columna Date.

1. En el objeto visual de matriz, elimine la jerarquía Products y luego reemplácela por la jerarquía Calendar.

1. Agregue una columna calculada a la tabla Sales:

```dax
Cost = 'Sales'[Quantity] * RELATED('Product'[Cost])
```

1. Aplíquele formato a la columna Cost con dos decimales.

## Creación de una medida rápida

1. Agregue una medida rápida a la tabla Sales, restando la columna Cost de la columna Profit.

1. Cambie el nombre de la medida a Profit.

1. Explique que la medida no almacena datos en el modelo.

Creación de medidas regulares

1. Agregue una medida a la tabla Sales:

```dax
Profit Margin = DIVIDE([Profit], SUM('Sales'[Sales]))
```

1. Aplíquele formato a la columna Profit Margin como un porcentaje.

1. Agregue otra medida a la tabla Sales:

```dax
Sales YTD = TOTALYTD(SUM('Sales'[Sales]), 'Date'[Date])
```

1. Aplíquele formato a la columna Sales YTD con dos decimales.

## Validación de los cálculos con el objeto visual de matriz

1. Agregue los campos Cost, Profit, Profit Margin y Sales YTD al objeto visual de matriz.

1. Guarde el archivo de Power BI Desktop.

1. Deje el archivo de Power BI Desktop abierto para una demostración posterior.
