---
demo:
  title: Administración de archivos y modelos semánticos en Power BI
  module: Deploy and manage Power BI service items
---
# Administración de archivos y modelos semánticos en Power BI

## Preparación para la actualización de datos de la puerta de enlace

> **Tenga en cuenta** que los siguientes pasos no son necesarios cuando se utiliza la puerta de enlace de datos en modo personal. Puede pasar directamente al siguiente objetivo (configurar la puerta de enlace).

1. En Power BI Desktop, abra la ventana del Editor de Power Query y seleccione la consulta **ProductCost**.

1. Edite el paso Origen y, a continuación, modifique la ruta de acceso del archivo para usar el recurso compartido de archivos de la siguiente manera:

    `\\DATA-AI\Data\ProductCost.xlsx`

1. Cierre y aplique la ventana del Editor de Power Query.

1. Guarde el archivo de Power BI Desktop.

1. Publicar el archivo de Power BI Desktop en el área de trabajo, sobrescribiendo el modelo semántico y el informe en el servicio.

## Configuración de la puerta de enlace (modo personal)

1. En el servicio de Power BI para el instructor, recarga (F5) la página de configuración del modelo semántico.

1. Expande la sección Conexión de puerta de enlace e indica que no hay ninguna puerta de enlace instalada.

1. Utilice la lista desplegable de descargas (ubicada en la parte superior derecha) y seleccione Puerta de enlace de datos.

1. En la nueva página web, descargue la puerta de enlace en modo personal.

1. Una vez descargado, abra el archivo que ha descargado.

1. Complete la configuración de la puerta de enlace mediante las credenciales de la cuenta del instructor.

1. Una vez configurada, regresa y recarga la página de configuración del modelo semántico.

1. Asigne la puerta de enlace personal y edite las credenciales de los dos orígenes de datos.

1. Para ambos orígenes de datos, establezca el método de autenticación en **WindowsWithoutImpersonation** y el nivel de privacidad en **Organizativo**.

1. Opcionalmente, expanda la sección **Actualización programada** y muestre cómo configurar un programa recurrente.

## Actualizar el modelo semántico

1. Antes de actualizar el modelo semántico, abre el panel **Supervisión de ventas**.

1. Edita los detalles del icono Ventas, Margen de beneficio para mostrar la hora de la última actualización.

1. Haga clic con el botón derecho en el archivo `D:\Allfiles\Demo\Resources\UpdateDatabase-LoadAdditionalSales.ps1`y, a continuación, ejecute con PowerShell. *Este script cargará los datos de ventas de diciembre de 2020 en la base de datos.*

1. En el servicio Power BI para el instructor, en el panel de navegación, actualiza el modelo semántico del **Análisis de ventas**.

1. Cuando se complete la actualización, indique cómo aparece la columna del icono del panel **Diciembre 2020** y que la hora de actualización es **AHORA**.
