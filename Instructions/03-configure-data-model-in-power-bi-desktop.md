---
lab:
  title: Modelado de datos en Power BI Desktop
  module: Module 4 - Design a Data Model in Power BI
ms.openlocfilehash: 1617d6a1a50e37a5dc7d9094eaa86057b2ddeee2
ms.sourcegitcommit: 9ea1e7e21b9b3c718030c94b1693d153a2010ec7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2022
ms.locfileid: "147015369"
---
# <a name="model-data-in-power-bi-desktop"></a>**Modelado de datos en Power BI Desktop**

**El tiempo estimado para completar el laboratorio es de 45 minutos.**

En este laboratorio, comenzará a desarrollar el modelo de datos. Implicará la creación de relaciones entre las tablas y, después, la configuración de las propiedades de tabla y columna para mejorar la facilidad de uso del modelo de datos. También creará jerarquías y medidas rápidas.

En este laboratorio, aprenderá a realizar lo siguiente:

- Crear relaciones de modelos

- Configurar propiedades de tablas y columnas

- Crear jerarquías


### <a name="lab-story"></a>**Caso de laboratorio**

Este laboratorio es una de las muchas series de laboratorios que se diseñaron como una historia completa sobre la preparación de datos para publicarlos como informes y paneles. Puede completar los laboratorios en cualquier orden. Sin embargo, si piensa trabajar en varios de ellos, le recomendamos que siga el orden siguiente:

1. Preparación de datos en Power BI Desktop

2. Carga de datos en Power BI Desktop

3. **Modelado de datos en Power BI Desktop**

5. Creación de cálculos DAX en Power BI Desktop, parte 1

6. Creación de cálculos DAX en Power BI Desktop, parte 2

7. Diseño de un informe en Power BI Desktop, parte 1

8. Diseño de un informe en Power BI Desktop, parte 2

9. Creación de un panel de Power BI

10. Análisis de datos en Power BI Desktop

11. Aplicación de seguridad de nivel de fila

## <a name="exercise-1-create-model-relationships"></a>**Ejercicio 1: Creación de relaciones del modelo**

En este ejercicio, creará relaciones del modelo.

### <a name="task-1-get-started"></a>**Tarea 1: Primeros pasos**

En esta tarea configurará el entorno para el laboratorio.

*Importante: Si viene de realizar el laboratorio anterior (y lo completó correctamente) no realice esta tarea; en su lugar, continúe con la siguiente.*

1. Para abrir Power BI Desktop, en la barra de tareas, haga clic en el acceso directo de Microsoft Power BI Desktop.

    ![Imagen 12](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image1.png)

1. Para cerrar la ventana de introducción, en la parte superior izquierda de la ventana, haga clic en **X**.

    ![Imagen 11](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image2.png)

1. Para abrir el archivo de inicio de Power BI Desktop, haga clic en la ficha de cinta **Archivo** a fin de abrir la vista Backstage.

1. Seleccione **Abrir informe**.

    ![Imagen 10](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image3.png)

1. Haga clic en **Examinar informes**.

    ![Imagen 8](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image4.png)

1. En la ventana **Abrir**, vaya a la carpeta **D:\PL300\Labs\03-configure-data-model-in-power-bi-desktop\Starter**.

1. Seleccione el archivo **Sales Analysis**.

1. Haga clic en **Abrir**.

    ![Imagen 7](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image5.png)

1. Cierre todas las ventanas informativas que se abran.

1. Para crear una copia del archivo, haga clic en la ficha de cinta **Archivo** para abrir la vista Backstage.

1. Seleccione **Guardar como**.

    ![Imagen 5](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image6.png)

1. Si se le pide que aplique los cambios, haga clic en **Aplicar**.

    ![Imagen 15](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image7.png)

1. En la ventana **Guardar como**, vaya a la carpeta **D:\PL300\MySolution**.

1. Haga clic en **Guardar**.

    ![Imagen 3](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image8.png)

### <a name="task-2-create-model-relationships"></a>**Tarea 2: Creación de relaciones del modelo**

En esta tarea, creará relaciones del modelo.

1. En Power BI Desktop, en la parte izquierda, haga clic en el icono de la vista **Modelo**.

    ![Imagen 1](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image9.png)

2. Si no ve las siete tablas, desplácese horizontalmente hacia la derecha y, después, arrastre y junte las tablas para poder verlas todas al mismo tiempo.

    *Sugerencia: También puede utilizar el control de zoom situado en la parte inferior de la ventana.*

    *En la vista Modelo, se pueden ver las tablas y las relaciones (conectores entre tablas). Actualmente no hay ninguna relación porque deshabilitó las opciones de relación de carga de datos en el laboratorio **Preparación de datos en Power BI Desktop**.*

3. Para volver a la vista Informe, a la izquierda, haga clic en el icono de la vista **Informe**.

    ![Imagen 327](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image10.png)

4. Para ver todos los campos de tabla, en el panel **Campos**, haga clic con el botón derecho en un área vacía y, después, seleccione **Expandir todo**.

    ![Imagen 328](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image11.png)

5. Para crear un objeto visual de tabla, en el panel **Campos**, desde dentro de la tabla **Product** (Producto), active el campo **Categoría**.

    ![Imagen 329](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image12.png)

    *Los laboratorios usan una notación abreviada para hacer referencia a un campo. Tendrá este aspecto: **Producto \| Categoría**. En este ejemplo, **Product** es el nombre de la tabla y **Category** es el nombre del campo.*

6. Para agregar una columna adicional a la tabla, en el panel **Campos**, active el campo **Sales \| Sales** (Ventas | Ventas).

7. Observe que en el objeto visual de tabla se enumeran cuatro categorías de productos y que el importe de ventas es el mismo para cada una de ellas, y el mismo para el total.

    ![Imagen 330](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image13.png)

    *El problema es que la tabla se basa en campos de otras tablas. La expectativa es que en cada categoría de producto se muestren las ventas de esa categoría. Pero como no hay una relación del modelo entre estas tablas, la tabla **Sales** (Ventas) no se filtra. Ahora agregará una relación para propagar los filtros entre las tablas.*

8. En la pestaña **Modelado** de la cinta, en el grupo **Relaciones**, haga clic en **Administrar relaciones**.

    ![Imagen 331](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image14.png)

9. En la ventana **Administrar relaciones**, observe que todavía no se ha definido ninguna relación.

10. Para crear una relación, haga clic en **Nueva**.

    ![Imagen 332](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image15.png)

11. En la ventana **Crear relación**, en la primera lista desplegable, seleccione la tabla **Product** (Producto).

    ![Imagen 333](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image16.png)

12. En la segunda lista desplegable (bajo la cuadrícula de la tabla **Product**), seleccione la tabla **Sales** (Ventas).

    ![Imagen 334](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image17.png)

13. Observe que se han seleccionado automáticamente las columnas **ProductKey** (Clave de producto) de cada tabla.

    *Las columnas se han seleccionado porque comparten los mismos nombre y tipo de datos.*

14. En la lista desplegable **Cardinalidad**, observe que se ha seleccionado **Uno a varios (1:*)**.

    *La cardinalidad se ha detectado de forma automática, ya que Power BI entiende que la columna **ProductKey** de la tabla **Product** contiene valores únicos. Las relaciones uno a varios son la cardinalidad más común y todas las relaciones que cree en este laboratorio serán de este tipo.*

15. En la lista desplegable **Dirección del filtro cruzado**, observe que está seleccionado el valor **Único**.

    *La dirección de filtro único significa que los filtros se propagan de "un lado" a "varios lados". En este caso, significa que los filtros que se aplican a la tabla **Product** se propagarán a la tabla **Sales**, pero no en la dirección contraria.*

16. Observe que la opción **Mark This Relationship Active** (Marcar esta relación activa) está seleccionada.

    *Las relaciones activas propagan los filtros. Una relación se puede marcar como inactiva para que los filtros no se propaguen. Pueden existir relaciones inactivas cuando hay varias rutas de relación entre las tablas. En este caso, los cálculos del modelo pueden usar funciones especiales para activarlas.*

17. Haga clic en **Aceptar**.

    ![Imagen 335](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image18.png)

18. En la ventana **Administrar relaciones**, observe que aparece la nueva relación y, después, haga clic en **Cerrar**.

    ![Imagen 336](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image19.png)

19. En el informe, observe que el objeto visual de tabla se ha actualizado a fin de mostrar valores diferentes para cada categoría de producto.

    ![Imagen 337](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image20.png)

    *Los filtros que se aplican a la tabla **Product** ahora se propagan a la tabla **Sales**.*

20. Cambie a la vista Modelo y observe que ahora hay un conector entre las dos tablas (no importa si las tablas están situadas unas junto a otras).

    ![Imagen 338](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image21.png)

21. En el diagrama, observe que puede interpretar la cardinalidad, que la representan los indicadores **1** y *****.

    *La dirección del filtro se representa mediante la punta de la flecha. Una línea continua representa una relación activa; una línea discontinua representa una relación inactiva.*

22. Mantenga el cursor sobre la relación para resaltar las columnas relacionadas.

    *Hay una manera más fácil de crear una relación. En el diagrama del modelo, puede arrastrar y colocar columnas para crear una relación.*

23. Para crear una relación mediante una técnica distinta, en la tabla **Reseller** (Revendedor), arrastre la columna **ResellerKey** (Clave de revendedor) a la columna **ResellerKey** de la tabla **Sales**.

    ![Imagen 339](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image22.png)

    *Sugerencia: A veces una columna no se deja arrastrar. Si se produce esta situación, seleccione otra columna y, después, vuelva a seleccionar la columna que quiere arrastrar e inténtelo de nuevo. Cerciórese de que se ve la nueva relación agregada al diagrama.*

24. Use la técnica nueva para crear las dos relaciones de modelo siguientes:

    - De **Region \| SalesTerritoryKey** (Región | Clave de territorio de ventas) a **Sales \| SalesTerritoryKey** (Ventas | Clave de territorio de ventas)

    - De **Salesperson \| EmployeeKey** (Vendedor | Clave de empleado) a **Sales \| EmployeeKey** (Ventas | Clave de empleado)

25. En el diagrama, organice las tablas para que la tabla **Sales** se coloque en el centro del diagrama y las tablas relacionadas estén organizadas a su alrededor. Coloque las tablas desconectadas al lado.

    ![Imagen 340](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image23.png)


26. Guarde el archivo de Power BI Desktop.

## <a name="exercise-2-configure-tables"></a>**Ejercicio 2: Configuración de tablas**

En este ejercicio, para configurar cada tabla creará jerarquías y ocultará, aplicará formato y clasificará las columnas.

### <a name="task-1-configure-the-product-table"></a>**Tarea 1: Configuración de la tabla Product**

En esta tarea, configurará la tabla **Product**.

1. En la vista Modelo, en el panel **Campos**, expanda la tabla **Product** si es necesario para mostrar todos los campos.

2. Para crear una jerarquía, en el panel **Campos**, haga clic con el botón derecho en la columna **Categoría** y, después, seleccione **Crear jerarquía**.

    ![Imagen 341](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image24.png)

3. En el panel **Propiedades** (a la izquierda del panel **Campos**), reemplace el texto en el cuadro **Nombre** con **Products**.

    ![Imagen 344](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image25.png)

4. Para agregar el segundo nivel de jerarquía, en el panel **Propiedades**, en la lista desplegable **Jerarquía**, seleccione **Subcategoría** (es posible que tenga que desplazarse hacia abajo dentro del panel).

5. Para agregar el tercer nivel a la jerarquía, seleccione **Product** en la lista desplegable **Jerarquía**.

6. Para completar el diseño de la jerarquía, haga clic en **Aplicar cambios en el nivel**.

    ![Imagen 343](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image26.png)

    *Sugerencia: No olvide hacer clic en **Aplicar cambios en el nivel**; es un error común pasar por alto este paso.*

7. En el panel **Campos**, observe la jerarquía **Products**.

    ![Imagen 347](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image27.png)

8. Para mostrar los niveles de la jerarquía, expanda la jerarquía **Products**.

    ![Imagen 346](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image28.png)

9. Para organizar las columnas en una carpeta para mostrar, seleccione primero la columna **Formato de color de fondo** en el panel **Campos**.

10. Mientras presiona la tecla **Ctrl**, seleccione la columna **Formato de color de fuente**.

11. En el panel **Propiedades**, en el cuadro **Carpeta para mostrar**, escriba **Formato**.

    ![Imagen 348](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image29.png)

12. En el panel **Campos**, observe que ahora las dos columnas están dentro de una carpeta.

    ![Imagen 349](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image30.png)

    *Las carpetas para mostrar son una excelente manera de descongestionar las tablas, especialmente las que contienen muchos campos.*

### <a name="task-2-configure-the-region-table"></a>**Tarea 2: Configuración de la tabla Region**

En esta tarea, configurará la tabla **Region**.

1. En la tabla **Region**, cree una jerarquía denominada **Regions** (Regiones), con los tres niveles siguientes:

    - Group (Grupo)

    - Country (País)

    - Region

    ![Imagen 350](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image31.png)

2. Seleccione la columna **Country** (País) (no el nivel de jerarquía **Country**).

3. En el panel **Propiedades**, expanda la sección **Avanzado** en la parte inferior del panel y, después, en la lista desplegable **Categoría de datos**, seleccione **País o región**.

    ![Imagen 352](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image32.png)

    *La categorización de datos puede proporcionar sugerencias al diseñador de informes. En este caso, la categorización de la columna como país o región proporciona información más precisa a Power BI cuando representa una visualización de mapa.*

### <a name="task-3-configure-the-reseller-table"></a>**Tarea 3: Configuración de la tabla Reseller**

En esta tarea, se configurará la tabla **Reseller**.

1. En la tabla **Reseller**, cree una jerarquía denominada **Resellers**, con los dos niveles siguientes:

    - Business Type

    - Reseller

    ![Imagen 351](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image33.png)

2. Cree una segunda jerarquía denominada **Geography** (Geografía), con los cuatro niveles siguientes:

    - Country-Region

    - State-Province

    - City

    - Reseller

    ![Imagen 353](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image34.png)

3. Establezca la **Categoría de datos** para las columnas **Country-Region**, **State-Province** y **City** (no el nivel de jerarquía) en **País o región**, **Estado o Provincia**, y **Ciudad**, respectivamente. 

### <a name="task-4-configure-the-sales-table"></a>**Tarea 4: Configuración de la tabla Sales**

En esta tarea, se configurará la tabla **Sales**.

1. En la tabla **Sales**, seleccione la columna **Cost**.

2. En el panel **Propiedades**, en el cuadro **Descripción**, escriba: **Basado en el costo estándar**

    ![Imagen 358](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image35.png)

    *Las descripciones se pueden aplicar a tablas, columnas, jerarquías o medidas. En el panel **Campos**, el texto descriptivo se muestra en una información sobre herramientas cuando el autor del informe mantiene el cursor sobre el campo.*

3. Seleccione la columna **Cantidad**.

4. En el panel **Propiedades**, dentro de la sección **Formato**, deslice la propiedad **Separador de miles** a **Sí**.

    ![Imagen 357](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image36.png)

5. Seleccione la columna **Precio unitario**.

6. En el panel **Propiedades**, desde dentro de la sección **Formato**, establezca la propiedad **Posiciones decimales** en **2**.

7. En el grupo **Avanzado** (es posible que tenga que desplazarse hacia abajo para encontrarlo), en la lista desplegable **Resumir por**, seleccione **Promedio**.

    ![Imagen 354](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image37.png)

    *De forma predeterminada, las columnas numéricas se resumen mediante la suma de valores. Este comportamiento predeterminado no es adecuado para una columna como **Precio unitario**, que representa una tarifa. Al establecer el resumen predeterminado en promedio se generará un resultado significativo.*

### <a name="task-5-bulk-update-properties"></a>**Tarea 5: Actualización masiva de propiedades**

En esta tarea, actualizará varias columnas mediante actualizaciones únicas masivas. Usará este enfoque para ocultar columnas y dar formato a los valores de columna.

1. En el panel **Campos**, seleccione la columna **Product \| ProductKey**.

2. Mientras presiona la tecla **Ctrl**, seleccione las 13 columnas siguientes (que abarcan varias tablas):

    - Region \| SalesTerritoryKey

    - Reseller \| ResellerKey

    - Sales \| EmployeeKey
    
    - Ventas \| ProductKey

    - Sales \| ResellerKey

    - Sales \| SalesOrderNumber

    - Sales \| SalesTerritoryKey

    - Salesperson \| EmployeeID

    - Salesperson \| EmployeeKey

    - Salesperson \| UPN

    - SalespersonRegion \| EmployeeKey

    - SalespersonRegion \| SalesTerritoryKey

    - Targets \| EmployeeID

3. En el panel **Propiedades**, deslice la propiedad **Está oculta** a **Sí**.

    ![Imagen 355](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image38.png)

    *Las columnas estaban ocultas porque las usan las relaciones, o se usarán en la configuración de seguridad de nivel de fila o en la lógica de cálculo.*

    *Usará **SalesOrderNumber** en un cálculo en el laboratorio **Creación de cálculos DAX en Power BI Desktop, parte 1**.*

4. Seleccione las tres columnas siguientes:

    - Product \| Standard Cost

    - Sales \| Cost

    - Sales \| Sales

5. En el panel **Propiedades**, desde dentro de la sección **Formato**, establezca la propiedad **Posiciones decimales** en **0**.

    ![Imagen 356](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image39.png)

## <a name="exercise-3-review-the-model-interface"></a>**Ejercicio 3: Revisión de la interfaz del modelo**

En este ejercicio, cambiará a la vista Informe y revisará la interfaz del modelo.

### <a name="task-1-review-the-model-interface"></a>**Tarea 1: Revisión de la interfaz del modelo**

En esta tarea, cambiará a la vista Informe y revisará la interfaz del modelo.

1. Cambio a la vista Informe.

2. En el panel **Campos**, observe lo siguiente:

    - Las columnas, las jerarquías y sus niveles son campos, que se pueden usar para configurar los objetos visuales del informe

    - Solo se ven los campos relevantes para la creación de informes

    - La tabla **SalespersonRegion** no es visible porque todos sus campos están ocultos

    - Los campos espaciales de la tabla **Region** y **Reseller** se etiquetan con un icono espacial

    - Los campos con la etiqueta sigma (Ʃ) se resumirán, de forma predeterminada

    - Aparece una información sobre herramientas al mantener el cursor sobre el campo **Sales \| Cost** (Ventas | Costo).

3. Expanda el campo **Sales \| OrderDate** (Ventas | Fecha de pedido) y, después, observe que muestra una jerarquía de fecha.

    ![Imagen 359](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image40.png)

    *El campo **Targets \| TargetMonth** (Destinos | Mes de destino) presenta una jerarquía similar. Estas jerarquías no las ha creado. Se han creado de forma automática. Pero hay un problema. El año fiscal de Adventure Works comienza el 1 de julio de cada año. Pero en estas jerarquías de fechas creadas automáticamente, la jerarquía de fecha comienza el 1 de enero de cada año.*

    *Ahora se desactivará este comportamiento automático. En el laboratorio **Creación de cálculos DAX en Power BI Desktop, parte 1**, usará DAX para crear una tabla de fechas y configurarla para definir el calendario de Adventure Works.*

4. Para desactivar la fecha y hora automáticas, haga clic en la ficha **Archivo** de la cinta para abrir la vista Backstage.

5. A la izquierda, elija **Opciones y configuración** y seleccione **Opciones**.

    ![Imagen 360](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image41.png)

6. En la ventana **Opciones**, a la izquierda, en el grupo **Archivo actual**, seleccione **Carga de datos**.

    ![Imagen 361](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image42.png)

7. En la sección **Inteligencia de tiempo**, desactive **Fecha y hora automáticas**.

    ![Imagen 362](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image43.png)

8. Haga clic en **Aceptar**.

    ![Imagen 9](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image44.png)

9. En el panel **Campos**, observe que las jerarquías de fecha ya no están disponibles.

    ![Imagen 363](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image45.png)


## <a name="exercise-4-create-quick-measures"></a>**Ejercicio 4: Creación de medidas rápidas**

En este ejercicio creará dos medidas rápidas.

### <a name="task-1-create-quick-measures"></a>**Tarea 1: Creación de medidas rápidas**

En esta tarea, creará dos medidas rápidas para calcular los beneficios y el margen de beneficio.

1. En el panel **Campos**, haga clic con el botón derecho en la tabla **Sales** y seleccione **Nueva medida rápida**.

    ![Imagen 366](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image46.png)

2. En la ventana **Medidas rápidas**, en la lista desplegable **Cálculo**, en el grupo **Operaciones matemáticas**, seleccione **Resta**.

    ![Imagen 367](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image47.png)

3. En el panel **Campos** de la ventana **Medidas rápidas**, expanda la tabla **Sales**.

4. Arrastre el campo **Sales** al cuadro **Valor base**.

5. Arrastre el campo **Costo** al cuadro **Valor que se restará**.

    ![Imagen 368](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image48.png)

6. Haga clic en **Aceptar**.

    ![Imagen 369](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image49.png)

    *Una medida rápida crea el una fórmula de cálculo de forma automática. Son fáciles y rápidas de crear para cálculos simples y comunes. Creará medidas sin usar esta herramienta en el laboratorio **Creación de cálculos DAX en Power BI Desktop, parte 1**.*

7. En el panel **Campos**, dentro de la tabla **Sales**, observe la nueva medida.

    ![Imagen 370](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image50.png)

    *Las medidas se adornan con el icono de una calculadora.*

8. Para cambiar el nombre de la medida, haga clic con el botón derecho en ella y, después, seleccione **Cambiar nombre**.

    ![Imagen 371](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image51.png)

    *Sugerencia: Para cambiar el nombre de un campo, también puede hacer doble clic en él, o bien seleccionarlo y presionar **F2**.*

9. Cambie el nombre de la medida por **Beneficio** y, después, presione **Entrar**.

10. En la tabla **Sales**, agregue una segunda medida rápida, en función de los requisitos siguientes:

    - Use la operación matemática **División**.

    - Establezca el **Numerador** en el campo **Sales \| Profit**.

    - Establezca el **Denominador** en el campo **Sales \| Sales**.

    - Cambie el nombre de la medida por **Margen de beneficio**.

    ![Imagen 372](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image52.png)

    ![Imagen 373](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image53.png)

11. Asegúrese de que la medida **Margen de beneficio** está seleccionada y, después, en la cinta contextual **Herramientas de medición**, establezca el formato en **Porcentaje**, con dos posiciones decimales.

    ![Imagen 374](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image54.png)

12. Para probar las dos medidas, primero seleccione el objeto visual de tabla en la página del informe.

13. En el panel **Campos**, active las dos medidas.

    ![Imagen 375](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image55.png)

14. Haga clic en la guía de la derecha y arrástrela para ampliar el objeto visual de tabla.

    ![Imagen 376](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image56.png)

15. Compruebe que las medidas generan un resultado razonable con el formato correcto.

    ![Imagen 378](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image57.png)

### <a name="task-2-create-a-many-to-many-relationship"></a>**Tarea 2: Creación de una relación de varios a varios**

En esta tarea, creará una relación de varios a varios entre las tablas **Salesperson** y **Sales**.

1. En Power BI Desktop, en la vista Informe, en el panel **Campos**, active los dos campos siguientes para crear un objeto visual de tabla:

    - Salesperson \| Salesperson

    - Sales \| Sales

    *Los laboratorios usan una notación abreviada para hacer referencia a un campo. Tendrá este aspecto: **Salesperson \| Salesperson**. En este ejemplo, **Salesperson** es el nombre de la tabla y **Salesperson** es el nombre del campo.*

    ![Imagen 1](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image9.png)

    *En la tabla se muestran las ventas realizadas por cada vendedor. Pero hay otra relación entre los vendedores y las ventas. Algunos vendedores pertenecen a una, dos o posiblemente más regiones de ventas. Además, las regiones de ventas pueden tener varios vendedores asignados.*

    *Desde la perspectiva de la administración del rendimiento, las ventas de un vendedor (en función de sus territorios asignados) se deben analizar y comparar con los objetivos de ventas. Creará relaciones para admitir este análisis en el siguiente ejercicio.*

2. Observe que Michael Blythe ha vendido casi 9 millones USD.

3. Cambie a la vista Modelo.

    ![Imagen 10](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image10.png)

4. Arrastre la tabla **SalespersonRegion** para colocarla entre las tablas **Region** y **Salesperson**.

5. Use la técnica de arrastrar y colocar para crear las dos relaciones de modelo siguientes:

    - De **Salesperson \| EmployeeKey** a **SalespersonRegion \| EmployeeKey**

    - De **Region \| SalesTerritoryKey** a **SalespersonRegion \| SalesTerritoryKey**

    *La tabla **SalespersonRegion** se puede considerar una tabla de puente.*

6. Cambie a la vista Informe y, después, observe que el objeto visual no se ha actualizado: el resultado de ventas de Michael Blythe no ha cambiado.

7. Vuelva a la vista Modelo y, luego, siga la dirección del filtro de relación (la punta de flecha) desde la tabla **Salesperson**.

    *Tenga en cuenta lo siguiente: la tabla **Salesperson** filtra la tabla **Sales**. También filtra la tabla **SalespersonRegion**, pero no continúa hasta la tabla **Region** (la flecha apunta a la dirección equivocada).*

    ![Imagen 380](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image11.png)

8. Para editar la relación entre las tablas **Region** y **SalespersonRegion**, haga doble clic en la relación.

9. En la ventana **Editar relación**, en la lista desplegable **Dirección del filtro cruzado**, seleccione **Ambos**.

10. Active la casilla **Aplicar filtro de seguridad en ambas direcciones**.

    ![Imagen 381](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image12.png)

11. Haga clic en **Aceptar**.

    ![Imagen 335](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image13.png)

12. Observe que la relación tiene una flecha doble.

    ![Imagen 382](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image14.png)

13. Cambie a la vista Informe y, después, observe que los valores de ventas todavía no han cambiado.

    *Ahora el problema está relacionado con el hecho de que hay dos posibles rutas de propagación del filtro entre las tablas **Salesperson** y **Sales**. Esta ambigüedad se resuelve de manera interna, en función de una evaluación del "número mínimo de tablas". Para ser claros, no debería diseñar modelos con este tipo de ambigüedad, el problema se solucionará en parte más adelante en este laboratorio y al completar el laboratorio **Creación de cálculos DAX en Power BI Desktop, parte 1**.*

14. Cambie a la vista Modelo.

15. Para forzar la propagación del filtro a través de la tabla de puente, edite (haga doble clic en) la relación entre las tablas **Salesperson** y **Sales**.

16. En la ventana **Editar relación**, desactive la casilla **Activar esta relación**.

    ![Imagen 383](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image15.png)

17. Haga clic en **Aceptar**.

    ![Imagen 5696](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image16.png)

    *Ahora la propagación del filtro seguirá la única ruta activa.*

18. En el diagrama, observe que la relación inactiva se representa mediante una línea discontinua.

    ![Imagen 5697](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image17.png)

19. Cambie a la vista Informe y, después, observe que las ventas de Michael Blythe ahora ascienden casi a 22 millones USD.

    ![Imagen 5698](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image18.png)

20. Observe también que las ventas de cada vendedor, si se sumaran, superarían el total de la tabla.

    *Es una observación común de una relación de varios a varios, debido al recuento doble, triple, etc., de los resultados de las ventas regionales. Fíjese en Brian Welcker, el segundo vendedor de la lista. Su importe de ventas es igual a la cantidad total de ventas. Es el resultado correcto simplemente debido a que es el director de ventas; sus ventas se miden por las de todas las regiones.*

    *Aunque la relación de varios a varios ya funciona, ahora no se pueden analizar las ventas realizadas por un vendedor (porque la relación está inactiva). Podrá reactivar la relación al introducir una tabla calculada que permitirá el análisis de ventas realizado en las regiones de ventas asignadas al vendedor (para un análisis del rendimiento) en el laboratorio **Creación de cálculos DAX en Power BI Desktop, parte 1**.*

21. Cambie a la vista Modelado y, después, en el diagrama, seleccione la tabla **Salesperson**.

22. En el panel **Propiedades**, en el cuadro **Nombre**, reemplace el texto por **Salesperson (Performance)** (Vendedor (rendimiento)).

    *La tabla con el nombre cambiado ahora refleja su finalidad: se usa para notificar y analizar el rendimiento de los vendedores en función de las ventas de sus regiones de ventas asignadas.*

### <a name="task-3-relate-the-targets-table"></a>**Tarea 3: Relación con la tabla Targets**

En esta tarea, creará una relación con la tabla **Targets**.

1. Cree una relación desde la columna **Salesperson (Performance) \| EmployeeID** y la columna **Targets \| EmployeeID**.

2. En la vista Informe, agregue el campo **Targets \| Target** al objeto visual de tabla.

3. Cambie el tamaño del objeto visual de tabla para que todas las columnas estén visibles.

    ![Imagen 5699](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image19.png)

    *Ahora se pueden visualizar las ventas y los destinos, pero debe tener cuidado por dos motivos. En primer lugar, no hay ningún filtro en un período de tiempo, por lo que los destinos también incluyen cantidades de destino futuras. En segundo lugar, los destinos no son aditivos y, por tanto, no se debe mostrar el total. Se pueden deshabilitar dándole formato al objeto visual, o bien quitarse mediante la lógica de cálculo. Seguirá el segundo enfoque mediante la creación de una medida de destino en el laboratorio **Creación de cálculos DAX en Power BI Desktop, parte 2**, que devolverán EN BLANCO cuando se filtre más de un vendedor.*

### <a name="task-4-finish-up"></a>**Tarea 4: Finalización**

En esta tarea, completará el laboratorio.

1. Guarde el archivo de Power BI Desktop.

2. Si se le pide que aplique las consultas, haga clic en **Aplicar más tarde**.

3. Si quiere iniciar el siguiente laboratorio, deje Power BI Desktop abierto.
