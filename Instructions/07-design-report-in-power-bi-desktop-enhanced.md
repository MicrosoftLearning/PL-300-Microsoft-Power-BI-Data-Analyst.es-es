---
lab:
  title: "Mejora de un informe en Power\_BI Desktop"
  module: Create Reports in Power BI desktop
---


# Mejora de un informe en Power BI Desktop

## **Caso de laboratorio**

En este laboratorio, mejorará el **análisis de ventas** con características de diseño avanzadas.

En este laboratorio, aprenderá a:

- Sincronizar segmentaciones
- Creación de una página de obtención de detalles
- Aplicar formato condicional
- Crear y usar marcadores

**Este laboratorio debe durar unos 45 minutos**.

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

## **Introducción y apertura del informe**

En esta tarea, configurará el entorno para el laboratorio abriendo el informe de inicio.

*Importante: Si ha realizado el laboratorio anterior (y lo ha completado correctamente) no realice esta tarea; en su lugar, pase a la siguiente.*

1. Abra Power BI Desktop.

    ![Icono de Power BI Desktop](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image1.png)

    *Sugerencia: De forma predeterminada, se abre el cuadro de diálogo Introducción delante de Power BI Desktop. Puede optar por iniciar sesión y cerrar la ventana emergente.*

1. Para abrir el archivo de inicio de Power BI Desktop, seleccione **Archivo > Abrir informe > Examinar informes**.

1. En la ventana **Abrir**, vaya a la carpeta **D:\PL300\Labs\07-design-report-in-power-bi-desktop-enhanced\Starter** y abra el archivo **Sales Analysis**.

1. Cierre todas las ventanas informativas que se abran.

1. Fíjese en el mensaje de advertencia amarillo bajo la cinta.

    *Este mensaje le avisa de que no se han aplicado consultas para cargar el archivo como tablas de modelo. Aplicará consultas más adelante en este laboratorio.*

    *Para descartar el mensaje de advertencia, a la derecha del mensaje de advertencia en amarillo, seleccione la **X**.*

1. Para crear una copia del archivo, vaya a **Archivo > Guardar como** y guárdelo en la carpeta **D:\PL300\MySolution**.

1. Si se le pide que aplique los cambios, seleccione **Aplicar más tarde**.

## **Sincronizar segmentaciones**

En esta tarea, sincronizará las segmentaciones **Año** y **Región**, continuando con el desarrollo del informe creado en el laboratorio **Diseñar un informe en Power BI Desktop** laboratorio.

1. En Power BI Desktop, en la página **Información general**, establezca la segmentación **Año** en **FY2018**.

1. Vaya a la página **Mi rendimiento** y, después, observe que la segmentación **Año** es otro valor.

    *Cuando las segmentaciones no están sincronizadas, pueden contribuir a la representación errónea de los datos y a la frustración de los usuarios del informe. Ahora sincronizará las segmentaciones del informe.*

1. Vuelva a la página **Información general** y, después, seleccione la segmentación **Año**.

1. En la ficha de cinta **Ver**, desde el grupo **Mostrar paneles**, seleccione **Sincronizar segmentaciones**.

     ![Imagen 1](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image13.png)

1. En el panel **Segmentaciones de sincronización** (a la izquierda del panel **Visualizaciones**), en la segunda columna (que representa la sincronización), active las casillas de las páginas **Información general** y **Mi rendimiento**.

     ![Imagen 93](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image14.png)

1. En la página **Información general**, seleccione la segmentación **Región**.

1. Sincronice la segmentación con las páginas **Información general** y **Beneficios**.

     ![Imagen 94](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image15.png)

1. Para probar las segmentaciones de sincronización, seleccione otras opciones de filtrado y, después, compruebe que las segmentaciones sincronizadas filtran por la misma selección.

1. Para cerrar la página **Sincronizar segmentaciones**, seleccione la **X** situada en la parte superior derecha del panel.

## **Configuración de la obtención de detalles**

En este ejercicio, creará una página y la configurará como una página de obtención de detalles. Cuando haya completado el diseño, la página tendrá un aspecto similar al siguiente:

![Imagen de la página nueva, que consta de un objeto visual de tarjeta y un objeto visual de tabla.](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image17.png)

## **Creación de una página de obtención de detalles**

En esta tarea, creará una página y la configurará como una página de obtención de detalles.

1. Agregue una nueva página de informe con el nombre **Detalles del producto**.

1. Haga clic con el botón derecho en la pestaña de la página **Detalles del producto** y después seleccione **Ocultar página**.

    *Los usuarios del informe no podrán ir directamente a la página de obtención de detalles. Tendrán que acceder a ella desde objetos visuales en otras páginas. En el ejercicio final de este laboratorio descubrirá cómo obtener detalles de la página.*

1. Debajo del panel **Visualizaciones**, en la sección **Obtener detalles**, agregue el campo **Producto \| Categoría** al cuadro **Add Drill-Through Fields Here** (Agregar los campos de obtención de detalles aquí).

    *Los laboratorios usan una notación abreviada para hacer referencia a un campo. Tendrá este aspecto: **Producto \| Categoría**. En este ejemplo, **Product** es el nombre de la tabla y **Category** es el nombre del campo.*

     ![Imagen 96](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image20.png)

1. Para probar la página de obtención de detalles, en la tarjeta de filtro de obtención de detalles, seleccione **Bikes** (Bicicletas).

     ![Imagen 99](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image21.png)

1. En la parte superior izquierda de la página del informe, observe el botón de flecha.

    *Un botón de flecha se agrega automáticamente cuando se agrega un campo al apartado o área de obtención de detalles. Permite a los usuarios del informe retroceder a la página desde la que han obtenido detalles.*

1. Agregue un objeto visual **Tarjeta** a la página y, después, cambie el tamaño y colóquelo para ubicarlo a la derecha del botón y rellenar el ancho restante de la página.

    ![Imagen 13](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image23.png)

    ![Imagen 101](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image24.png)

1. Arrastre el campo **Producto \| Categoría** al objeto visual de tarjeta.

1. Configure las opciones de formato para el objeto visual y, después, establezca la propiedad **Etiqueta de categoría** en **Desactivar**.

     ![Imagen 103](Linked_image_Files/07-design-report-in-power-bi-desktop_image36b.png)

1. Establezca la propiedad **Efectos > Color de fondo** en un tono gris claro, como *Blanco, 20 % más oscuro*.

     ![Imagen 103](Linked_image_Files/07-design-report-in-power-bi-desktop_image36c.png)

1. Agregue un objeto visual **Tabla** a la página y, después, cambie el tamaño y colóquelo para ubicarlo debajo del objeto visual de tarjeta y rellenar el espacio restante de la página.

     ![Imagen 14](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image26.png)

     ![Imagen 105](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image27.png)

1. Agregue los campos siguientes al objeto visual:

     - Producto \| Subcategoría
     - Producto \| Color
     - Ventas \| Cantidad
     - Ventas \| Ventas
     - Ventas \| Margen de beneficio

1. Configure las opciones de formato para el objeto visual y, en la sección **Valores**, establezca la propiedad **Tamaño de texto** en **20pt**.

*El diseño de la página de obtención de detalles está casi terminado. En el siguiente ejercicio mejorará la página con formato condicional.*

## **Adición de formato condicional**

En este ejercicio, mejorará la página de obtención de detalles con formato condicional. Cuando haya completado el diseño, la página tendrá un aspecto similar al siguiente:

![Imagen de una página actualizada, que muestra iconos y valores con formato de color.](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image28.png)

## **Adición de formato condicional**

En esta tarea, mejorará la página de obtención de detalles con formato condicional.

1. Seleccione el objeto visual de tabla. En el panel de visualización, seleccione la flecha hacia abajo del valor **Margen de beneficio** y, después, seleccione **Formato condicional \| Iconos**.

    ![Imagen 107](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image29.png)

1. En la ventana **Iconos: Margen de beneficio**, en la lista desplegable **Diseño de los iconos**, seleccione **A la derecha de los datos**.

     ![Imagen 108](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image30.png)

1. Para eliminar la regla intermedia, a la derecha del triángulo amarillo, seleccione la **X**.

     ![Imagen 109](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image31.png)

1. Configure la primera regla (el rombo de color rojo) de esta manera:

    - En el segundo control, quite el valor
    - En el tercer control, seleccione **Número**
    - En el quinto control, escriba **0**
    - En el sexto control, seleccione **Número**

1. Configure la segunda regla (el círculo de color verde) de esta manera y, a continuación, seleccione **Aceptar**:

    *Las reglas se pueden interpretar de la siguiente manera: mostrar un rombo de color rojo si el valor de margen de beneficio es menor que 0; de lo contrario, si el valor es mayor o igual a cero, mostrar un círculo de color verde.*

     - En el segundo control, escriba **0**
     - En el tercer control, seleccione **Número**
     - En el quinto control, quite el valor
     - En el sexto control, seleccione **Número**

     ![Imagen 110](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image32.png)

1. En el objeto visual de tabla, compruebe que se muestran los iconos correctos.

     ![Imagen 112](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image34.png)

1. Configure el formato condicional de color de fondo para el campo **Color**.

1. En la ventana **Color de fondo: Color**, en la lista desplegable **Estilo de formato**, seleccione **Valor de campo**.

1. En la lista desplegable **¿En qué campo debemos basar esto?** , seleccione **Producto \| Formato \| Formato del color de fondo** y, a continuación, **Aceptar**.

     ![Imagen 114](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image36.png)

1. Repita los pasos anteriores para configurar el formato condicional de color de fuente para el campo **Color**, mediante el campo **Producto \| Formato \| Formato de color de fondo**.

*Puede que recuerde que los colores de fondo y fuente se crearon a partir del archivo **ColorFormats.csv** en el laboratorio **Preparación de datos de Power BI Desktop** y, después, se integraron en la consulta **Producto** en el laboratorio **Carga de datos en Power BI Desktop**.*

## **Adición de marcadores y botones**

En este ejercicio, mejorará la página **Mi rendimiento** con botones, lo que permite al usuario del informe seleccionar el tipo de objeto visual que se va a mostrar. Cuando haya completado el diseño, la página tendrá un aspecto similar al siguiente:

![Imagen de una página 3 actualizada, en la que se muestran dos botones y ahora solo dos objetos visuales.](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image38.png)

## **Adición de marcadores**

En esta tarea, agregará dos marcadores, para mostrar cada uno de los objetos visuales de ventas mensuales y destinos.

1. Vaya a la página **Mi rendimiento**. En la ficha de cinta **Ver**, desde el grupo **Mostrar paneles**, seleccione **Marcadores**.

     ![Imagen 118](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image39.png)

1. En la ficha de cinta **Ver**, desde el grupo **Mostrar paneles**, seleccione **Selección**.

1. En el panel **Selección**, situado junto a uno de los elementos **Ventas y destino por mes**, seleccione el icono de ojo para ocultar el objeto visual.

     ![Imagen 120](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image41.png)

1. En el panel **Marcadores**, haga clic en **Agregar**.

    *Para cambiar el nombre del marcador, haga doble clic en él.*

     ![Imagen 121](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image42.png)

1. Si el gráfico visible es el gráfico de barras, cambie el nombre del marcador por **Gráfico de barras ACTIVADO**, de lo contrario cámbielo por **Gráfico de columnas ACTIVADO**.

1. Para editar el marcador, en el panel **Marcadores**, desplace el cursor sobre el marcador, seleccione los puntos suspensivos y, a continuación, seleccione **Datos**.
     
     *Deshabilitar la opción **Datos** significa que el marcador no usará el estado de filtro actual. Esto es importante porque, de lo contrario, el marcador se bloqueará permanentemente en el filtro aplicado actualmente por la segmentación **Año**.*

     ![Imagen 16](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image43.png)

1. Para actualizar el marcador, seleccione los puntos suspensivos de nuevo y, a continuación, seleccione **Actualizar**.

     *En los pasos siguientes, creará y configurará un segundo marcador para mostrar el segundo objeto visual.*

1. En el panel **Selección**, alterne la visibilidad de los dos elementos **Ventas y destino por mes**.

     *En otras palabras, oculte el objeto visual visible y haga visible el objeto visual oculto.*

     ![Imagen 122](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image45.png)

1. Cree un segundo marcador y asígnele el nombre apropiado (**Gráfico de columnas ACTIVADO** o **Gráfico de barras ACTIVADO).**

     ![Imagen 123](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image46.png)

1. Configure el segundo marcador para omitir los filtros (opción **Datos** desactivada) y actualizar el marcador.

1. En el panel **Selección**, para que los dos objetos visuales sean visibles, basta con mostrar el objeto visual oculto.

1. Cambie el tamaño y la posición de los dos objetos visuales para que rellenen la página debajo del objeto visual de tarjeta de varias filas y se superpongan por completo.

    *Para seleccionar el objeto visual que está oculto, selecciónelo en el panel **Selección**.*

    ![Imagen 124](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image47.png)

1. En el panel **Marcadores**, seleccione cada uno de los marcadores y observe que solo uno de los objetos visuales es visible.

*La siguiente fase de diseño consiste en agregar dos botones a la página, lo que permitirá al usuario del informe seleccionar los marcadores.*

## **Agregar botones**

En esta tarea, agregará dos botones y les asignará acciones de marcador.

1. En la cinta **Insertar**, desde el grupo **Elementos**, seleccione **Botón** y, después, seleccione **En blanco**.

     ![Imagen 125](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image48.png)

1. Coloque el botón directamente debajo de la segmentación **Año**.

1. Seleccione el botón y, después, en el panel **Botón de formato**, seleccione **Botón**, expanda la sección **Estilo** y establezca la propiedad **Texto** del botón en **Activado**.

     ![Imagen 126](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image49b.png)

1. Expanda la sección **Texto** y, a continuación, en el cuadro **Texto**, escriba **Gráfico de barras**.

1. Expanda la sección **Rellenar** y, a continuación, establezca un color de fondo mediante un color complementario.

1. Seleccione **Botón** y establezca la propiedad **Acción** en **Activado**.

    ![Imagen 127](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image50.png)

1. Expanda la sección **Acción** y, después, establezca la lista desplegable **Tipo** en **Marcador**.

1. En la lista desplegable **Marcador**, seleccione **Gráfico de barras ACTIVADO**.

    ![Imagen 128](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image51.png)

1. Cree una copia del botón mediante copiar y pegar y, después, configure el botón nuevo de la siguiente manera:

    *Sugerencia: Los comandos de acceso directo para copiar y pegar son **Ctrl+C** seguido de **Ctrl+V**.*

    - Establezca la propiedad **Texto del botón** en **Gráfico de columnas**.
    - En la sección **Acción**, establezca la lista desplegable **Marcador** en **Gráfico de columnas ACTIVADO**.

*Ahora se ha completado el diseño del informe Sales Analysis.*

## **Publicación del informe**

En esta tarea, publicará el informe.

1. Seleccione la página **Información general**.

1. En la segmentación **Año**, seleccione **FY2020**.

1. En la segmentación **Región**, seleccione **Seleccionar todo**.

1. Guarde el archivo de Power BI Desktop.

    *El archivo se debe guardar siempre antes de publicarlo en el servicio Power BI.*

1. En la pestaña de la cinta **Inicio**, en el grupo **Compartir**, seleccione **Publicar**.

     ![Imagen 21](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image52.png)

1. En la ventana **Publicar en Power BI**, observe que **Mi área de trabajo** esté seleccionado.

1. Para publicar el informe, elija **Seleccionar**.
    1. Si se le pide que reemplace el conjunto de datos, seleccione **Reemplazar**.
    1. Cuando la publicación se haya realizado correctamente, seleccione **Entendido**.

1. Cierre Power BI Desktop.

*En el siguiente ejercicio, explorará el informe en el servicio Power BI.*

## **Exploración del informe**

En esta tarea, explorará el informe en el servicio Power BI.

1. En una ventana del explorador Microsoft Edge, vaya al servicio Power BI > **Mi área de trabajo** y seleccione el informe **Análisis de ventas**.

1. Para probar la característica de obtención de detalles, vaya a la página **Información general** > objeto visual **Cantidad por categoría** . A continuación, haga clic con el botón derecho en la barra **Ropa** y seleccione **Obtener detalles \| Detalles del producto**.

     ![Imagen 130](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image55.png)

1. Observe que la página **Detalles del producto** es para **Clothing**.

1. Para volver a la página de origen, seleccione el botón de flecha en la esquina superior izquierda de la página.

1. Seleccione la página **Mi rendimiento**.

    *Seleccione cada uno de los botones y, después, observe que se muestra otro objeto visual.*

### **Finalización**

En esta tarea, completará el laboratorio.

Para volver al área de trabajo, en el banner de la página web de la ventana, seleccione **Mi área de trabajo**.

![Imagen 23](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image56.png)
