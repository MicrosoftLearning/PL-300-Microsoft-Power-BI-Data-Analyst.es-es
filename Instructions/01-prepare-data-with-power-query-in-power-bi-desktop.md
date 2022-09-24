---
lab:
  title: "Preparación de datos en Power\_BI Desktop"
  module: Module 2 - Get Data in Power BI
---

# <a name="prepare-data-in-power-bi-desktop"></a>**Preparación de datos en Power BI Desktop**

**El tiempo estimado para completar el laboratorio es de 45 minutos.**

In this lab you commence the development of a Power BI Desktop solution for the Adventure Works company. It involves connecting to source data, previewing the data, and using data preview techniques to understand the characteristics and quality of the source data.

En este laboratorio, aprenderá a:

- Abrir Power BI Desktop

- Establecer las opciones de Power BI Desktop

- Conectar con datos de origen

- Obtener una vista previa de los datos de origen

- Usar técnicas de vista previa de datos para entender mejor los datos

### <a name="lab-story"></a>**Caso de laboratorio**

This lab is one of many in a series of labs that was designed as a complete story from data preparation to publication as reports and dashboards. You can complete the labs in any order. However, if you intend to work through multiple labs, for the first 10 labs, we suggest you do them in the following order:

1. **Preparación de datos en Power BI Desktop**

2. Carga de datos en Power BI Desktop

3. Modelado de datos en Power BI Desktop

5. Creación de cálculos DAX en Power BI Desktop, parte 1

6. Creación de cálculos DAX en Power BI Desktop, parte 2

7. Diseño de un informe en Power BI Desktop, parte 1

8. Diseño de un informe en Power BI Desktop, parte 2

9. Creación de un panel de Power BI

10. Análisis de datos en Power BI Desktop

11. Aplicación de seguridad de nivel de fila

## <a name="exercise-1-prepare-data"></a>**Ejercicio 1: Preparación de los datos**

In this exercise you will create eight Power BI Desktop queries. Six queries will source data from SQL Server, and two from CSV files.

### <a name="task-1-save-the-power-bi-desktop-file"></a>**Tarea 1: Guardado del archivo de Power BI Desktop**

En esta tarea, primero guardará el archivo de Power BI Desktop.

1. Para abrir Power BI Desktop, en la barra de tareas, haga clic en el acceso directo de Microsoft Power BI Desktop.

    ![Imagen 2](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image1.png)

1. Para cerrar la ventana de introducción, en la parte superior izquierda de la ventana, haga clic en la **X**.

    ![Imagen 3](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image2.png)

1. Para guardar el archivo, haga clic en la ficha de cinta **Archivo** a fin de abrir la vista Backstage.

1. Seleccione **Guardar**.

    ![Imagen 4](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image3.png)

1. En la ventana **Guardar como**, vaya a la carpeta **D:\PL300\MySolution**.

1. En el cuadro **Nombre de archivo**, escriba **Sales Analysis** (Análisis de ventas).

    ![Imagen 14](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image4.png)

1. Haga clic en **Guardar**.

    ![Imagen 17](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image5.png)

    Sugerencia: Para guardar el archivo, también puede hacer clic en el icono **Guardar** situado en la parte superior izquierda.

    ![Imagen 18](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image6.png)

### <a name="task-2-set-power-bi-desktop-options"></a>**Tarea 2: Establecimiento de las opciones de Power BI Desktop**

En esta tarea, establecerá las opciones de Power BI Desktop.

1. En Power BI Desktop, haga clic en la ficha de cinta **Archivo** para abrir la vista Backstage.

1. A la izquierda, elija **Opciones y configuración** y seleccione **Opciones**.

    ![Imagen 1](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image7.png)

1. En la ventana **Opciones**, a la izquierda, en el grupo **Archivo actual**, seleccione **Carga de datos**.

    ![Imagen 5](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image8.png)

    La configuración de **Carga de datos** para el archivo actual permite una serie de opciones que determinan los comportamientos predeterminados del modelado.

1. En el grupo **Relaciones**, desactive las dos opciones que están activadas.

    ![Imagen 7](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image9.png)

    While having these two options enabled can be helpful when developing a data model, you disabled them earlier to support the lab experience. When you create relationships in the <bpt id="p1">**</bpt>Load Data in Power BI Desktop<ept id="p1">**</ept> lab, you’ll learn why you are adding each one.

1. Haga clic en **Aceptar**.

    ![Imagen 9](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image10.png)

1. Guarde el archivo de Power BI Desktop.

### <a name="task-3-get-data-from-sql-server"></a>**Tarea 3: Obtención de datos de SQL Server**

En esta tarea, creará consultas basadas en tablas de SQL Server.

1. En la ficha de cinta **Inicio**, en el grupo **Datos**, haga clic en **SQL Server**.

    ![Imagen 19](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image11.png)

2. En la ventana **Base de datos de SQL Server**, en el cuadro **Servidor**, escriba **localhost**.

    ![Imagen 21](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image12.png)

    En este laboratorio, empezará a desarrollar una solución de Power BI Desktop para la empresa Adventure Works.

3. Haga clic en **Aceptar**.

    ![Imagen 22](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image13.png)

4. En la ventana **Navegador**, a la izquierda, expanda la base de datos **AdventureWorksDW2020**.

    A lo largo del proceso, conectará con datos de origen, obtendrá una vista previa de los datos y usará técnicas de vista previa de datos para comprender las características y la calidad de los datos de origen.

    ![Imagen 28](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image17.png)

5. Seleccione la tabla **DimEmployee**, pero no active su casilla.

    ![Imagen 29](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image18.png)

6. En el panel de la derecha, fíjese en que hay una vista previa de los datos de la tabla.

    Los datos de la vista previa permiten determinar las columnas y un ejemplo de filas.

7. Para crear consultas, active la casilla situada junto a las seis tablas siguientes:

    - DimEmployee

    - DimEmployeeSalesTerritory

    - DimProduct

    - DimReseller

    - DimSalesTerritory

    - FactResellerSales

8. Para aplicar transformaciones a los datos de las tablas seleccionadas, haga clic en **Transformar datos**.

    You won’t be transforming the data in this lab. The objectives of this lab focus on exploring and profiling the data in the <bpt id="p1">**</bpt>Power Query Editor<ept id="p1">**</ept> window.

    ![Imagen 30](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image19.png)

### <a name="task-4-preview-sql-server-queries"></a>**Tarea 4: Vista previa de las consultas de SQL Server**

In this task you will preview the data of the SQL Server queries. First, you will learn relevant information about the data. You will also use column quality, column distribution, and column profile tools to understand the data and to assess data quality.

1. En la ventana del **Editor de Power Query**, a la izquierda, observe el panel **Consultas**.

    ![Imagen 31](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image20.png)

    El panel **Consultas** contiene una consulta para cada tabla seleccionada.

2. Seleccione la primera consulta **DimEmployee**.

    ![Imagen 33](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image21.png)

    The <bpt id="p1">**</bpt>DimEmployee<ept id="p1">**</ept> table in the SQL Server database stores one row for each employee. A subset of the rows from this table represents the salespeople, which will be relevant to the model you’ll develop.

3. En la barra de estado de la parte inferior izquierda, observe las estadísticas de la tabla: 33 columnas y 296 filas.

    ![Imagen 36](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image22.png)

4. En el panel de vista previa de los datos, desplácese horizontalmente para revisar todas las columnas.

5. Observe que las cinco últimas columnas contienen vínculos de tipo **Tabla** o **Valor**.

    These five columns represent relationships to other tables in the database. They can be used to join tables together. You’ll join tables in the <bpt id="p1">**</bpt>Load Data in Power BI Desktop<ept id="p1">**</ept> lab.

6. Para evaluar la calidad de las columnas, en la ficha de cinta **Vista**, en el grupo **Vista previa de los datos**, consulte **Calidad de columnas**.

    ![Imagen 35](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image23.png)

    La característica calidad de las columnas permite determinar fácilmente el porcentaje de valores válidos, errores o valores vacíos encontrados en las columnas.

7. En la columna **Position** (sexta columna desde el final), observe que el 94 % de las filas están vacías (NULL).

    ![Imagen 38](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image24.png)

8. Para evaluar la distribución de las columnas, en la ficha de cinta **Vista**, en el grupo **Vista previa de los datos**, consulte **Distribución de columnas**.

    ![Imagen 40](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image25.png)

9. Revise de nuevo la columna **Position** y observe que hay cuatro valores distintos y uno único.

10. Revise la distribución de la columna **EmployeeKey** (la primera): 296 valores distintos y 296 únicos.

    ![Imagen 43](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image26.png)

    When the distinct and unique counts are the same, it means the column contains unique values. When modeling, it’s important that some model tables have unique columns. These unique columns can be used to create one-to-many relationships, which you will do in the <bpt id="p1">**</bpt>Model Data in Power BI Desktop, Part 1<ept id="p1">**</ept> lab.

11. En el panel **Consultas**, seleccione la consulta **DimEmployeeSalesTerritory**.

    ![Imagen 44](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image27.png)

    The <bpt id="p1">**</bpt>DimEmployeeSalesTerritory<ept id="p1">**</ept> table stores one row for each employee and the sales territory regions they manage. The table supports relating many regions to a single employee. Some employees manage one, two, or possibly more regions. When you model this data, you’ll need to define a many-to-many relationship, which you’ll do in the <bpt id="p1">**</bpt>Model Data in Power BI Desktop, Part 2<ept id="p1">**</ept> lab.

12. En el panel **Consultas**, seleccione la consulta **DimProduct**.

    ![Imagen 46](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image28.png)

    La tabla **DimProduct** contiene una fila por producto vendido por la empresa.

13. Desplácese horizontalmente para mostrar las últimas columnas.

14. Observe la columna **DimProductSubcategory**.

    Al agregar transformaciones a esta consulta en el laboratorio **Carga de datos en Power BI Desktop**, usará la columna **DimProductSubcategory** para combinar tablas.

15. En el panel **Consultas**, seleccione la consulta **DimReseller**.

    ![Imagen 49](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image29.png)

    The <bpt id="p1">**</bpt>DimReseller<ept id="p1">**</ept> table contains one row per reseller. Resellers sell, distribute, or value add to the Adventure Works products.

16. Para ver los valores de las columnas, en la ficha de cinta **Vista**, en el grupo **Vista previa de los datos**, consulte **Perfil de columna**.

    ![Imagen 41](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image30.png)

17. Seleccione el encabezado de columna **BusinessType**.

18. Observe el nuevo panel que hay debajo del panel de vista previa de los datos.

19. Revise las estadísticas de columna y la distribución de valores en el panel de vista previa de los datos.

20. Observe el problema en la calidad de los datos: hay dos etiquetas para el almacén (**Warehouse** y **Ware House**, este último mal escrito).

    ![Imagen 51](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image31.png)

21. Si mantiene el puntero sobre la barra de **Ware House**, verá que hay cinco filas con este valor.

    Aplicará una transformación para cambiar la etiqueta de estas cinco filas en el laboratorio **Carga de datos en Power BI Desktop**.

22. En el panel **Consultas**, seleccione la consulta **DimSalesTerritory**.

    ![Imagen 52](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image32.png)

    The <bpt id="p1">**</bpt>DimSalesTerritory<ept id="p1">**</ept> table contains one row per sales region, including <bpt id="p2">**</bpt>Corporate HQ<ept id="p2">**</ept> (headquarters). Regions are assigned to a country, and countries are assigned to groups. In the <bpt id="p1">**</bpt>Model Data in Power BI Desktop, Part 1<ept id="p1">**</ept> lab, you’ll create a hierarchy to support analysis at region, country, or group level.

23. En el panel **Consultas**, seleccione la consulta **FactResellerSales**.

    ![Imagen 54](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image33.png)

    La tabla **FactResellerSales** contiene una fila por línea de pedido de venta. Un pedido de venta contiene uno o varios elementos de línea.

24. Revise la calidad de la columna **TotalProductCost** y observe que el 8 % de las filas están vacías.

    ![Imagen 63](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image34.png)

    Este laboratorio es una de las muchas series de laboratorios que se diseñaron como una historia completa sobre la preparación de datos para publicarlos como informes y paneles.

### <a name="task-5-get-data-from-a-csv-file"></a>**Tarea 5: Obtención de datos de un archivo CSV**

En esta tarea, creará una consulta basada en un archivo CSV.

1. Para agregar una nueva consulta, vaya a la ventana **Editor de Power Query**. En la ficha de cinta **Inicio**, en el grupo **Nueva consulta**, haga clic en la flecha desplegable de **Nuevo origen** y luego seleccione **Texto o CSV**.

    ![Imagen 70](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image35.png)

2. En la ventana **Abrir**, vaya a la carpeta **D:\PL300\Resources** y seleccione el archivo **ResellerSalesTargets.csv**.

3. Haga clic en **Abrir**.

4. En la ventana **ResellerSalesTargets.csv**, revise la vista previa de los datos.

5. Haga clic en **Aceptar**.

    ![Imagen 71](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image36.png)

  
‎ 

6. En el panel **Consultas**, observe la adición de la consulta **ResellerSalesTargets**.

    ![Imagen 72](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image37.png)

    Puede completar los laboratorios en cualquier orden.

7. Observe que ninguna columna contiene valores vacíos.

    Cuando no hay un objetivo de ventas mensual, se almacena un carácter de guion.

8. Revise los iconos de cada encabezado de columna, a la izquierda del nombre de columna.

    ![Imagen 74](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image38.png)

    Sin embargo, si piensa trabajar en varios de ellos, para los diez primeros le recomendamos que siga el orden siguiente:

    Aplicará muchas transformaciones para lograr un resultado con forma diferente que solo conste de tres columnas (**Date**, **EmployeeKey** y **TargetAmount**) en el laboratorio **Carga de datos de Power BI Desktop**.

### <a name="task-6-get-additional-data-from-a-csv-file"></a>**Tarea 6: Obtención de datos adicionales de un archivo CSV**

En esta tarea, creará una consulta adicional basada en un archivo CSV diferente.

1. Siga los pasos de la tarea anterior para crear una consulta basada en el archivo **D:\PL300\Resources\ColorFormats.csv**.

    ![Imagen 75](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image39.png)

    The <bpt id="p1">**</bpt>ColorFormats<ept id="p1">**</ept> CSV file contains one row per product color. Each row records the HEX codes to format background and font colors. You’ll integrate this data with the <bpt id="p1">**</bpt>DimProduct<ept id="p1">**</ept> query data in the <bpt id="p2">**</bpt>Load Data in Power BI Desktop<ept id="p2">**</ept> lab.

### <a name="task-7-finish-up"></a>**Tarea 7: Finalización**

En esta tarea, completará el laboratorio.

1. En la ficha de cinta **Vista**, en el grupo **Vista previa de los datos**, desactive las tres opciones de vista previa de los datos que se habilitaron previamente en este laboratorio:

    - Calidad de columnas

    - Distribución de columnas

    - Perfil de columna

    ![Imagen 76](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image40.png)

2. Para guardar el archivo de Power BI Desktop, en la ventana del **Editor de Power Query**, en la vista Backstage de **Archivo**, seleccione **Guardar**.

    ![Imagen 77](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image41.png)

3. Cuando se le pida que aplique las consultas, haga clic en **Aplicar más tarde**.

    ![Imagen 86](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image42.png)

    Applying the queries will load their data to the data model. You’re not ready to do that, as there are many transformations that must be applied first.

4. Si quiere iniciar el siguiente laboratorio, deje Power BI Desktop abierto.

    Aplicará varias transformaciones a las consultas y, después, aplicará las consultas para cargarlas en el modelo de datos en el laboratorio **Carga de datos en Power BI Desktop**.
