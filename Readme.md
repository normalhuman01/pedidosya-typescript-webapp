# Pedidosya Webapp - Documentación

Este repositorio contiene el código fuente de la aplicación 'Pedidos Ya', que se ha dividido en dos aplicaciones separadas: una para el front-end y otra para el back-end. Esta división se ha realizado con el propósito de mantener una arquitectura modular que facilite el desarrollo y reduzca la detección de errores en el software. A continuación, se proporcionan detalles sobre la configuración y ejecución de ambas aplicaciones.

## Aplicación Back-End

La aplicación back-end se ha desarrollado utilizando Typescript, que luego se compila a JavaScript y se ejecuta en el entorno de Node.js. La elección de Typescript como lenguaje de desarrollo para ambas aplicaciones (back-end y front-end) se basa en su capacidad para reducir la incidencia de errores y acelerar el ciclo de desarrollo mediante la incorporación de un sistema de tipos estático. La compilación de Typescript a JavaScript se realiza utilizando el archivo 'gulpfile.js'.

### Configuración

Antes de ejecutar la aplicación, asegúrese de configurar las credenciales de 'clientId' y 'clientSecret' para acceder a la API de PedidoYa. Esta configuración se realiza en el archivo 'appConfig.ts' ubicado en la carpeta '.../Backend/server/config/'.

### Ejecución

Para poner en marcha la aplicación back-end, siga estos pasos:

1. Abra una terminal en su sistema.

2. Navegue hasta la carpeta '.../Backend/'.

3. Ejecute el comando `npm install` para instalar las dependencias del proyecto.

4. Utilice el comando `gulp build` para compilar el código Typescript a JavaScript.

5. Finalmente, inicie la aplicación del servidor con `node dist/app.js`.

## Aplicación Front-End

La aplicación front-end se ha construido utilizando el popular framework Angular. La elección de Angular se basa en su naturaleza gratuita y de código abierto, que facilita la creación de aplicaciones web de una sola página (SPA) y proporciona una amplia gama de herramientas y recursos para el desarrollo de interfaces de usuario interactivas y modernas.

### Configuración

No se requieren configuraciones adicionales para el front-end en este momento.

### Ejecución

Para ejecutar la aplicación front-end, siga estos pasos:

1. Abra una terminal en su sistema.

2. Navegue hasta la carpeta '.../Frontend/client'.

3. Ejecute el comando `npm install` para instalar las dependencias necesarias.

4. Inicie el servidor de desarrollo de Angular con `ng serve`.

## Puntos Pendientes

- **Mostrar Usuarios Logueados**:
  Para abordar la tarea de mostrar usuarios logueados, se propone mantener un registro de los usuarios en la base de datos, utilizando un indicador booleano que determine si están activos o no. Al iniciar sesión, se marcará al usuario como activo, y al cerrar la sesión, se marcará como inactivo. Además, se debe implementar un proceso interno que verifique a intervalos regulares el estado de los usuarios inactivos y los marque como inactivos si su sesión ha expirado sin un cierre de sesión adecuado. Esta estrategia garantizará un seguimiento preciso de los usuarios en línea y permitirá una gestión efectiva de las sesiones en la aplicación.
