---
lab:
  title: "Creación de un panel de Power\_BI"
  module: Create Dashboards
---

# Creación de un panel de Power BI

## Caso de laboratorio

En este laboratorio, creará el panel **Supervisión de ventas** en el servicio Power BI mediante un informe existente.

En este laboratorio, aprenderá a:

- Anclar objetos visuales en un panel
- Usar Preguntas y respuestas para crear iconos de panel

**Este laboratorio debe durar unos 30 minutos**.

## Introducción

Para completar este ejercicio, abre primero un explorador web e introduce la siguiente URL para descargar la carpeta zip:

`https://github.com/MicrosoftLearning/PL-300-Microsoft-Power-BI-Data-Analyst/raw/Main/Allfiles/Labs/09-create-power-bi-dashboard/09-create-dashboard.zip`

Extráela a la carpeta **C:\Users\Student\Downloads\09-create-dashboard**.

## **Publicación del informe**

En esta tarea, configurarás el entorno para el laboratorio creando un modelo semántico.

1. En la ventana del explorador Microsoft Edge, en el servicio Power BI, vaya a **Mi área de trabajo**.

1. Seleccione **Cargar > Examinar**.

1. Ve a la carpeta **C:\Users\Student\Downloads\09-create-dashboard**.

1. Selecciona el archivo **09-Starter-Sales Analysis.pbix** y luego, **Abrir**.

    > *Si se te pide que sustituyas el modelo semántico, selecciona **Sustituirlo**.*

## **Creación de un panel**

En esta tarea creará el panel **Supervisión de ventas**. Anclará un visual del informe y agregará un icono basado en un URI de datos de imagen, además de usar Preguntas y respuestas para crear un icono.

1. En el servicio Power BI, abre el informe **09-Starter-Sales Analysis**.

1. En la página **Información general**, establezca la segmentación **Año** en **FY2020**.

    ![Imagen 4](Linked_image_Files/09-create-power-bi-dashboard_image17.png)

1. Establezca la segmentación **Región** en **Seleccionar todo**.

    > *Los objetos visuales anclados se establecen con el contexto de filtro en el momento del anclaje. Si el objeto visual subyacente cambia, deberá actualizar también el icono del panel. En el caso de los filtros basados en el tiempo, es mejor usar una segmentación de fecha relativa (o Preguntas y respuestas usando una pregunta relativa basada en el tiempo).*

1. Para crear un panel y anclar un objeto visual, mantenga el cursor sobre el objeto visual (columna/línea) **Sales and Profit Margin by Month** y seleccione el pin.

    ![Imagen 43](Linked_image_Files/09-create-power-bi-dashboard_image18.png)

1. En la ventana **Anclar al panel**, en el cuadro **Nombre del panel**, escriba **Supervisión de ventas** y elija **Anclar**.

    ![Imagen 3](Linked_image_Files/09-create-power-bi-dashboard_image19.png)

1. Abra **Mi área de trabajo** y el panel **Supervisión de ventas**.

1. Observe que el panel tiene un solo icono.

    ![Imagen 45](Linked_image_Files/09-create-power-bi-dashboard_image22.png)

1. Para agregar un icono basado en una pregunta, en la parte superior izquierda del panel, seleccione **Pregunte algo sobre sus datos**. 

    *Puedes usar la característica de preguntas y respuestas para formular una pregunta, y Power BI responderá con un objeto visual.*

    ![Imagen 7](Linked_image_Files/09-create-power-bi-dashboard_image23.png)

1. Selecciona cualquiera de las preguntas sugeridas debajo del cuadro de preguntas y respuestas y revisa la respuesta.

1. Quite todo el texto del cuadro Preguntas y respuestas, y escriba lo siguiente: **Ventas hasta la fecha**.

1. Observe que la respuesta es **(En blanco)**.

    > *Quizás recuerdas que agregaste la medida **Ventas hasta la fecha** en el laboratorio **Creación de cálculos DAX avanzados en Power BI Desktop**. Esta medida es una expresión de inteligencia de tiempo y, por tanto, requiere un filtro en la tabla **Fecha** para generar un resultado.*

    ![Imagen 14](Linked_image_Files/09-create-power-bi-dashboard_image25.png)

1. Amplíe la pregunta con: **en el año FY2020**.

1. Observe que la respuesta ahora es **33 M USD**.

    ![Imagen 13](Linked_image_Files/09-create-power-bi-dashboard_image27.png)

1. Para anclar la respuesta al panel, en la esquina superior derecha, seleccione **Anclar visualización**.

    ![Imagen 15](Linked_image_Files/09-create-power-bi-dashboard_image28.png)

1. Cuando se te pida que ancles el icono al panel **Supervisión de ventas**, selecciona **Anclar**.

1. Para volver al panel, en la esquina superior izquierda, seleccione **Salir de Preguntas y respuestas**.

1. Para agregar el logotipo de la empresa, en la barra de menús, seleccione **Editar** y elija **Agregar icono**.
    
    > *El uso de esta técnica para agregar un icono le permite mejorar el panel con elementos multimedia, como contenido web, imágenes, cuadros de texto con formato enriquecido y vídeo (con vínculos de YouTube o Vimeo).*

1. En el panel **Agregar icono** (a la derecha), seleccione el icono **Imagen** y elija **Siguiente**.

1. En el panel **Agregar icono de imagen**, en el cuadro **URL**, escribe la dirección URL completa que se encuentra en el archivo **C:\Users\Student\Downloads\09-create-dashboard\AdventureWorksLogo_DataURL.txt** y selecciona **Aplicar**.
    
    > *Puede insertar una imagen mediante su dirección URL o puede usar una dirección URL de datos, que inserta el contenido en línea.*

1. Para cambiar el tamaño del icono del logotipo, arrastra la esquina inferior derecha y cambia el tamaño del icono a una unidad de ancho y una unidad de alto.
    
    > *El tamaño de los iconos está limitado a una forma rectangular.*

1. Organice los iconos de modo que el logotipo aparezca en la parte superior izquierda, con el icono **Ventas del año hasta la fecha** en la parte inferior, y el icono **Ventas, margen de beneficio**, en la parte derecha.

    ![Imagen 52](Linked_image_Files/09-create-power-bi-dashboard_image35.png)

## **Edición de los detalles del icono**

En esta tarea modificará los detalles de dos iconos.

1. Mantenga el cursor sobre el icono de **Ventas del año hasta la fecha** y, en la parte superior derecha del icono, seleccione los puntos suspensivos y, después, **Editar detalles**.

    ![Imagen 50](Linked_image_Files/09-create-power-bi-dashboard_image36.png)

1. En el panel **Detalles del icono** (a la derecha), en el cuadro **Subtítulo**, escriba **Año fiscal 2020** y seleccione **Aplicar**.

1. Observe que el icono **Ventas del año hasta la fecha** muestra un subtítulo.

    ![Imagen 21](Linked_image_Files/09-create-power-bi-dashboard_image39.png)

1. Edite los detalles del icono **Ventas, Margen de beneficio**.

1. En el panel **Detalles del icono**, en la sección **Funcionalidad**, active **Mostrar hora de última actualización** y elija **Aplicar**.

    ![Imagen 22](Linked_image_Files/09-create-power-bi-dashboard_image40.png)

1. Observe que el icono describe la hora de la última actualización (que se ha hecho al cargar el modelo de datos en Power BI Desktop).

*Debes actualizar el modelo semántico en el siguiente ejercicio. En función de tus datos y el informe, puedes hacer una actualización de datos ad hoc en cualquier momento o establecer una programación. Sin embargo, las actualizaciones programadas requieren puertas de enlace que no podemos configurar para este laboratorio. Por tanto, desde Power BI Desktop, debes realizar una actualización de datos manual y, posteriormente, cargar el archivo en tu área de trabajo.*

## **Actualiza el modelo semántico**

En este ejercicio, primero se cargarán los datos del pedidos de ventas de junio de 2020 en la base de datos **AdventureWorksDW2020**. A continuación, abrirá el archivo de Power BI Desktop, actualizará los datos y cargará el archivo en el área de trabajo.

> ***Nota**: Si no puedes conectarte a la base de datos, puedes usar el archivo **09-Solution-Sales-Analysis.pbix**. En lugar de actualizar la base de datos y el modelo semántico, carga el archivo de solución en **Mi área de trabajo** y ve los cambios a los que se hace referencia en las siguientes tareas.*

## **Actualización de la base de datos de laboratorio**

En esta tarea, se ejecutará un script de PowerShell para actualizar los datos de la base de datos **AdventureWorksDW2020**.

1. En el Explorador de archivos, dentro de la carpeta **C:\Users\Student\Downloads\09-create-dashboard**, haz clic con el botón derecho en el archivo **UpdateDatabase-2-AddSales.ps1** y, después, selecciona **Ejecutar con PowerShell**.

    ![Imagen 28](Linked_image_Files/09-create-power-bi-dashboard_image46.png)

1. Si se le solicita que cambie la directiva de ejecución, pulse **A**.

1. Cuando se le pida que presione cualquier tecla para cerrar, vuelva a presionar **Entrar**.

*La base de datos **AdventureWorksDW2020** ahora incluye los pedidos de ventas realizados en junio de 2020.*

## **Actualización del archivo de Power BI Desktop**

En esta tarea, abrirás el archivo **09-Starter-Sales Analysis** de Power BI Desktop, actualizarás los datos y cargarás el archivo en tu área de trabajo **Análisis de ventas**.

1. En el archivo de Power BI Desktop, en el panel **Datos**, haga clic con el botón derecho en la tabla **Ventas** y, a continuación, seleccione **Actualizar datos**.

    ![Imagen 55](Linked_image_Files/09-create-power-bi-dashboard_image47.png)

1. Cuando finalice la actualización, guarde el archivo de Power BI Desktop.

1. Para publicar el archivo en su área de trabajo, en la ficha de cinta **Inicio**, dentro del grupo **Compartir**, seleccione **Publicar** y, después, **Seleccionar**.

    ![Imagen 59](Linked_image_Files/09-create-power-bi-dashboard_image48.png)

1. Cuando se te solicite que sustituyas el modelo semántico, selecciona **Sustituir**.

1. Cierre Power BI Desktop.

*El modelo semántico en el servicio Power BI incluye ahora los datos de ventas de junio de 2020.*

### **Revisión del panel**

En esta tarea revisará el panel para ver las ventas actualizadas.

1. En la ventana del explorador Microsoft Edge, abra el servicio Power BI y revise el panel **Supervisión de ventas** en **Mi área de trabajo**.

2. En el icono **Ventas, margen de beneficio**, en el subtítulo, observe que los datos se han actualizado a **AHORA**.

3. Observe también que ahora hay una columna para **Junio de 2020**.

    > *Si no ve los datos de junio de 2020, es posible que tenga que presionar **F5** para volver a cargar el explorador web.*

    ![Imagen 33](Linked_image_Files/09-create-power-bi-dashboard_image50.png)

## Laboratorio completado
