---
lab:
  course: PL-300
  title: Realización de un análisis avanzado con objetos visuales de inteligencia artificial
  module: Perform Data Analysis in Power BI
---


# **Análisis de datos en Power BI**

## **Caso de laboratorio**

En este laboratorio, creará el informe **Exploración de ventas**.

En este laboratorio, aprenderá a:

- Crear gráficos de dispersión animados
- Usar un objeto visual para pronosticar valores

**Este laboratorio debe durar unos 30 minutos**.

## **Introducción e inicio de sesión**

En esta tarea configurará el entorno para el laboratorio iniciando sesión en Power BI.

*Nota: Si ya ha iniciado sesión en Power BI, pase a la siguiente tarea.*

1. Para abrir Microsoft Edge, en la barra de tareas, seleccione el acceso directo del programa Microsoft Edge.

     ![Imagen 12](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image1.png)

1. En la ventana del explorador Microsoft Edge, vaya a **https://app.powerbi.com**.

    *Sugerencia: También puede usar el favorito del servicio Power BI en la barra de favoritos de Microsoft Edge.*

1. Complete el proceso de inicio de sesión con las credenciales de su organización (o las que se le hayan proporcionado). Si Microsoft Edge le solicita si quiere mantener la sesión iniciada, seleccione **Sí**.

1. En la ventana del explorador Microsoft Edge, en el panel **Navegación** del servicio Power BI, expanda **Mi área de trabajo**. Deje abierta la ventana del explorador Microsoft Edge.

     ![Imagen 22](Linked_image_Files/07-my-workspace-new.png)

## **Introducción: crear un modelo semántico**

En esta tarea, configurarás el entorno para el laboratorio creando un modelo semántico. *Si ya has publicado el modelo semántico, pasa a la siguiente tarea.*

1. En la ventana del explorador Microsoft Edge, en el servicio Power BI, vaya a **Mi área de trabajo**.

1. Seleccione **Cargar > Examinar**.

1. Vaya a la carpeta **D:\Allfiles\Labs\08-perform-data-analysis-in-power-bi-desktop\Starter**.

1. Seleccione el archivo **Sales Analysis.pbix** y, a continuación, **Abrir**.

    *Si se te pide que sustituyas el modelo semántico, selecciona **Sustituirlo**.*

*Este método creará un informe y un modelo semántico. Solo usaremos el modelo semántico para crear un nuevo informe en este ejercicio. Este mismo proceso se puede realizar con un modelo semántico de otro informe en lugar de cargar uno nuevo. Además, si no usas el informe, los procedimientos recomendados del área de trabajo recomiendan eliminar el archivo innecesario.*

## **Creación del informe**

En esta tarea, crearás una conexión dinámica al modelo semántico de Power BI que creaste en la última tarea y, a continuación, crearás un nuevo informe de **Exploración de ventas**.

1. Abra Power BI Desktop.

    ![Icono de Power BI Desktop](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image1.png)

    *Importante: Si ya tiene Power BI Desktop abierto (de un laboratorio anterior), cierre esa instancia.*

    *Sugerencia: De forma predeterminada, se abre el cuadro de diálogo Introducción delante de Power BI Desktop. Puede optar por iniciar sesión y cerrar la ventana emergente.*

1. En la cinta de opciones Inicio, selecciona **Obtener datos > Modelos semánticos de Power BI**.

1. En la ventana **Centro de datos**, selecciona el modelo semántico de **Análisis de ventas** en **Mi área de trabajo** y luego  **Conectar**, o bien haz doble clic para cargar el modelo semántico.

1. Vaya a **Archivo > Guardar** y guarde el nombre de archivo como **Exploración de ventas** en la carpeta **D:\Allfiles\MySolution**.

*Ahora creará dos páginas de informe, y en cada una trabajará con un objeto visual diferente para analizar y explorar los datos.*

## **Creación de un gráfico de dispersión animado**

En esta tarea, creará un gráfico de dispersión que se puede animar.

1. Cambie el nombre **Página 1** por **Gráfico de dispersión**.

1. Agregue un objeto visual **Gráfico de dispersión** a la página del informe y, después, cambie su tamaño y colóquelo para que ocupe toda la página.
    
    *El gráfico se puede animar cuando se agrega un campo al apartado o área **Eje de reproducción**.*

     ![Imagen 18](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image15.png)

     ![Imagen 75](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image16.png)

1. Agregue los campos siguientes a los apartados o áreas del objeto visual:
    
    *Los laboratorios utilizan una notación abreviada para hacer referencia a un campo, con este formato: **Reseller** **\|** **Business Type**. En este ejemplo, **Reseller** es el nombre de la tabla y **Business Type** es el nombre del campo.*

     - Eje X: **Ventas \| Ventas**
     - Eje Y: **Ventas \| Margen de beneficio**
     - Leyenda: **Revendedor \| Tipo de negocio**
     - Tamaño: **Ventas \| Cantidad**
     - Eje de reproducción: **Fecha \| Trimestre**

1. En el panel **Filtros**, agregue el campo **Producto \| Categoría** al apartado o área **Filtros** de esta página.

1. En la tarjeta de filtro, filtre por **Bicicletas**.

1. Para animar el gráfico, en la esquina inferior izquierda, seleccione **Reproducir**.

    ![Imagen 41](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image19.png)

1. Vea todo el ciclo de animación desde **FY2018 Q1** hasta **FY2020 Q4**.
    
    *El gráfico de dispersión permite comprender los valores de medida de manera simultánea: en este caso, cantidad de pedido, ingresos de ventas y margen de beneficios.*
    
    *Cada burbuja representa un tipo de negocio de revendedor. Los cambios en el tamaño de la burbuja reflejan las cantidades de pedido mayores o menores. Los movimientos horizontales representan aumentos o disminuciones de los ingresos de ventas, y los movimientos verticales, aumentos o disminuciones de la rentabilidad.*

1. Cuando se detenga la animación, seleccione una de las burbujas para ver su seguimiento a lo largo del tiempo.

1. Mantenga el cursor sobre cualquier burbuja para mostrar una información sobre herramientas en la que se describen los valores de medida para el tipo de distribuidor en ese momento dado.

1. En el panel **Filtros**, filtre solo por **Clothing** (Ropa) y observe que genera un resultado muy diferente.

1. Guarde el archivo de Power BI Desktop.


## **Creación de una previsión**

En esta tarea creará una previsión para determinar los posibles ingresos de ventas futuros.

1. Agregue una nueva página y, después, cambie el nombre de la página por **Previsión**.

1. Agregue un objeto visual **Gráfico de líneas** a la página del informe y, después, cambie su tamaño y colóquelo para que ocupe toda la página.

     ![Imagen 19](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image21.png)

     ![Imagen 74](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image22.png)

1. Agregue los campos siguientes a los apartados o áreas del objeto visual:

     - Eje X: **Fecha \| Fecha**
     - Eje Y: **Ventas \| Ventas**

1. En el panel **Filtros**, agregue el campo **Fecha \| Año** al apartado o área **Filtros de esta página**.

1. En la tarjeta de filtro, filtre por dos años: **FY2019** y **FY2020**.
    
    *Al realizar la previsión sobre una línea temporal, necesitará al menos dos ciclos (años) de datos para generar una previsión precisa y estable.*

1. Agregue también el campo **Producto \| Categoría** al apartado o área **Filtros de esta página** y filtre por **Bikes**.

1. Para agregar una previsión, debajo del panel **Visualizaciones**, seleccione el panel **Analytics** (Análisis).

     ![Imagen 20](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image26.png)

8. Expanda la sección **Previsión**.
    
    *Si la sección **Previsión** no está disponible, probablemente se deba a que el objeto visual no se ha configurado correctamente. La previsión solo está disponible cuando se cumplen dos condiciones: el eje tiene un único campo de tipo fecha y solo hay un campo de valor.*

1. **Active** la opción **Previsión**.

1. Configure las siguientes propiedades de previsión y elija **Aplicar**:

    - Unidades: **Meses**
    - **Predecir duración**: 1 mes
    - Estacionalidad: **365**
    - Intervalo de confianza: **80 %**

    ![Imagen 52](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image29.png)

1. En el objeto visual de línea, observe que la previsión se ha ampliado un mes más allá de los datos del historial.
    
    *El área de color gris representa la confianza. Cuanto mayor sea la confianza, menos estable y, por tanto, menos precisa será la previsión.*
    
    *Cuando conozca la duración del ciclo, en este caso anual, debe especificar los puntos de estacionalidad. A veces podría ser semanal (7) o mensual (30).*

1. En el panel **Filtros**, filtre solo por **Ropa** y observe que genera un resultado diferente.

### **Finalizar**

En esta tarea completará el laboratorio en Power BI Desktop.

1. Seleccione la página **Gráfico de dispersión**.

1. Guarde el archivo de Power BI Desktop.

1. Para publicar el archivo en **Mi área de trabajo**, en la ficha de cinta **Inicio**, dentro del grupo **Compartir**, seleccione **Publicar** y, después, **Seleccionar**.

    ![Imagen 23](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image46.png)

1. Cierre Power BI Desktop.
