---
lab:
  title: Aplicación de seguridad de nivel de fila
  module: Module 13 - Row-Level Security
---


# <a name="enforce-row-level-security"></a>**Aplicación de seguridad de nivel de fila**

**El tiempo estimado para completar el laboratorio es de 45 minutos.**

In this lab you will create a many-to-many relationship between the <bpt id="p1">**</bpt>Salesperson<ept id="p1">**</ept> table and the <bpt id="p2">**</bpt>Sales<ept id="p2">**</ept> table. You will also enforce row-level security to ensure that a salesperson can only analyze sales data for their assigned region(s).

En este laboratorio, aprenderá a:

- Configurar relaciones de varios a varios

- Aplicar seguridad de nivel de fila

### <a name="lab-story"></a>**Caso de laboratorio**

This lab is one of many in a series of labs that was designed as a complete story from data preparation to publication as reports and dashboards. You can complete the labs in any order. However, if you intend to work through multiple labs, for the first 10 labs, we suggest you do them in the following order:

1. Preparación de datos en Power BI Desktop

2. Carga de datos en Power BI Desktop

3. Modelado de datos en Power BI Desktop

5. Creación de cálculos DAX en Power BI Desktop, parte 1

6. Creación de cálculos DAX en Power BI Desktop, parte 2

7. Diseño de un informe en Power BI Desktop, parte 1

8. Diseño de un informe en Power BI Desktop, parte 2

9. Creación de un panel de Power BI

10. Análisis de datos en Power BI Desktop

11. **Aplicación de seguridad de nivel de fila**

## <a name="exercise-1-enforce-row-level-security"></a>**Ejercicio 1: Aplicación de seguridad de nivel de fila**

En este ejercicio aplicará seguridad de nivel de fila para asegurarse de que los vendedores solo puedan ver las ventas realizadas en sus regiones asignadas.

### <a name="task-1-get-started"></a>**Tarea 1: Primeros pasos**

En esta tarea configurará el entorno para el laboratorio.

*Importante: Si viene de realizar el laboratorio anterior (y lo completó correctamente) no realice esta tarea; en su lugar, continúe con la siguiente.*

1. Para abrir Power BI Desktop, en la barra de tareas, haga clic en el acceso directo de Microsoft Power BI Desktop.

    ![Imagen 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)

1. Para cerrar la ventana de introducción, en la parte superior izquierda de la ventana, haga clic en **X**.

    ![Imagen 7](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image2.png)

1. Para abrir el archivo de inicio de Power BI Desktop, haga clic en la ficha de cinta **Archivo** a fin de abrir la vista Backstage.

1. Seleccione **Abrir informe**.

    ![Imagen 6](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image3.png)

1. Haga clic en **Examinar informes**.

    ![Imagen 5](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image4.png)

1. En la ventana **Abrir**, vaya a la carpeta **D:\PL300\Labs\12-row-level-security\Starter**.

1. Seleccione el archivo **Sales Analysis**.

1. Haga clic en **Abrir**.

    ![Imagen 4](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image5.png)

1. Cierre todas las ventanas informativas que se abran.

1. Para crear una copia del archivo, haga clic en la ficha de cinta **Archivo** para abrir la vista Backstage.

1. Seleccione **Guardar como**.

    ![Imagen 3](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image6.png)

1. Si se le pide que aplique los cambios, haga clic en **Aplicar**.

    ![Imagen 15](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image7.png)

1. En la ventana **Guardar como**, vaya a la carpeta **D:\PL300\MySolution**.

1. Haga clic en **Guardar**.

    ![Imagen 2](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image8.png)

### <a name="task-2-enforce-row-level-security"></a>**Tarea 2: Aplicación de seguridad de nivel de fila**

En esta tarea aplicará seguridad de nivel de fila para asegurarse de que los vendedores solo puedan ver las ventas realizadas en sus regiones asignadas.

1. Cambie a la vista de datos.

    ![Imagen 5701](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image20.png)

2. En el panel **Campos**, seleccione la tabla **Salesperson (Performance)** (Vendedor [Rendimiento]).

3. Revise los datos y verá que Michael Blythe (EmployeeKey 281) tiene un valor de UPN de **michael-blythe@adventureworks.com** .

    *Recuerde que Michael Blythe está asignado a tres regiones de ventas: Noreste de EE. UU., Centro de EE. UU. y Sudeste de EE. UU.*

4. Cambie a la vista Informe.

5. En la ficha de cinta **Modelado**, en el grupo **Seguridad**, haga clic en **Administrar roles**.

    ![Imagen 5700](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image21.png)

6. En la ventana **Administrar roles**, haga clic en **Crear**.

    ![Imagen 5702](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image22.png)

7. En el cuadro, reemplace el texto seleccionado por el nombre del rol: **Salespeople** y, después, presione **Entrar**.

    ![Imagen 5703](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image23.png)

8. A fin de asignar un filtro para la tabla **Salesperson (Performance)** , haga clic en el carácter de puntos suspensivos (...) y, después, seleccione **Agregar filtro \| [UPN]** .

    ![Imagen 5704](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image24.png)

9. En el cuadro **Expresión DAX de filtro de tabla**, modifique la expresión reemplazando **"Value"** por **USERPRINCIPALNAME()** .

    ![Imagen 11](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image25.png)

    *USERPRINCIPALNAME() es una función de expresiones de análisis de datos (DAX) que devuelve el nombre del usuario autenticado. Significa que la tabla **Salesperson (Performance)** filtrará por el nombre principal de usuario (UPN) del usuario que realiza la consulta del modelo.*

10. Haga clic en **Guardar**.

    ![Imagen 5706](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image26.png)

11. Para probar el rol de seguridad, en la ficha de cinta **Modelado**, en el grupo **Seguridad**, haga clic en **Ver como**.

    ![Imagen 5708](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image27.png)

12. En la ventana **Ver como roles**, compruebe el elemento **Otro usuario** y, después, en el cuadro correspondiente, escriba **michael-blythe@adventureworks.com** .

13. Compruebe el rol **Salespeople**.

    ![Imagen 5709](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image28.png)

    *Esta configuración da como resultado el uso del rol **Salespeople** y la suplantación del usuario con el nombre Michael Blythe.*

14. Haga clic en **OK**.

    ![Imagen 5710](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image29.png)

15. Fíjese en el mensaje emergente amarillo, encima de la página del informe, que describe el contexto de seguridad de la prueba.

    ![Imagen 13](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image30.png)

16. En el objeto visual de tabla, observe que solo aparece el vendedor **Michael Blythe**.

    ![Imagen 5713](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image31.png)

17. Para detener las pruebas, en el lado derecho del banner amarillo, haga clic en **Detener visualización**.

    ![Imagen 5712](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image32.png)

    *Cuando el archivo de Power BI Desktop se publique en el servicio Power BI, deberá completar una tarea posterior a la publicación para asignar las entidades de seguridad al rol **Salespeople**. No lo haremos en este laboratorio.*

18. Para eliminar el rol, en la ficha de cinta **Modelado**, en el grupo **Seguridad**, haga clic en **Administrar roles**.

    ![Imagen 16](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image33.png)

19. En la ventana **Administrar roles**, haga clic en **Eliminar**.

    ![Imagen 17](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image34.png)

20. Cuando se le pida que confirme la eliminación, haga clic en **Sí, eliminar**.

21. Haga clic en **Guardar**.

    ![Imagen 18](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image35.png)

### <a name="task-2-finish-up"></a>**Tarea 2: Finalización**

En esta tarea, completará el laboratorio.

1. Guarde el archivo de Power BI Desktop.
