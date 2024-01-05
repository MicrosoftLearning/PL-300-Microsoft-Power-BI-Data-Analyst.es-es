---
demo:
  title: "Implementación de seguridad a nivel de fila en Power\_BI"
  module: Deploy and manage Power BI service items
---

# Implementación de seguridad a nivel de fila en Power BI

## Adición de una tabla de seguridad al modelo

1. En Power BI Desktop, abra la ventana Editor de Power Query.

1. Agregue una nueva consulta basada en el archivo `D:\Demo\Data\**ManagerCategory**.xlsx`.

1. Use la tabla **ManagerCategory** en el archivo.

1. Elimine la columna **Manager**.

1. Divida la columna **Categoría** por el delimitador de punto y coma y divídala en filas (opciones avanzadas).

1. En la columna **Email**, reemplace el valor **<ty-johnston@tailspintoys.com>** por la cuenta del destinatario (del archivo MySettings.txt).

1. Señale que este usuario puede ver tres categorías de productos: **Collective pitch, Trainer y Warbird**.

1. Cierre y aplique las consultas.

1. En la vista Modelo, cree una relación entre las tablas **ManagerCategory** y Product relacionando la columna **Category**.

1. Establezca la dirección del filtro cruzado en Único (**ManagerCategory** filtra Product).

1. Oculte la tabla **ManagerCategory**.

## Agregar un rol

1. En la vista Informe, abra Administrar roles y cree un rol denominado **Manager**.

1. En el rol, filtra la columna Dirección de correo electrónico de la tabla **ManagerCategory** de la siguiente manera:

  ```dax
   [Email] = USERPRINCIPALNAME()
   ```

1. **Guardar**

## Validación del rol

1. Abra Ver como y luego configure los siguientes ajustes:

    - Otro usuario: verifica y luego escribe la cuenta del destinatario.

    - Rol de administrador: Comprobación

1. Señale que el objeto visual de filtro muestra solo tres categorías de productos.

1. Deje de ver el informe usando las opciones de ver como.

1. Guarde el archivo de Power BI Desktop.

1. Publicar el archivo de Power BI Desktop en el área de trabajo, sobrescribiendo el modelo semántico y el informe en el servicio.

1. Cierre Power BI Desktop.

## Configuración de la seguridad del modelo semántico

1. En el servicio Power BI para el instructor, en el panel de navegación, abre la página de seguridad para el modelo semántico del **Análisis de ventas**.

1. En la sección Miembros, escriba la cuenta del destinatario (que representa a **Ty Johnston**).

1. Agréguela y guarde los cambios.

## Prueba de la seguridad de nivel de fila en la aplicación

1. En el servicio Power BI para el destinatario, actualice el panel (que se dejó abierto desde la demostración anterior).

1. En el icono del panel **Profit Margin**, compruebe que solo se ven tres categorías de productos.
