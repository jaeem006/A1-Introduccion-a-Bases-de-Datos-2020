[`Introducción a Bases de Datos`](../../Readme.md) > [`Sesión 04`](../Readme.md) > Ejemplo 00

## Ejemplo 0: Inicialización de servidores locales

### 1. Objetivos :dart: 
- Inicializar un servidor local de MySql

### 2. Requisitos :clipboard:
- __MySQL__ instalado en la computadora.

### 3. Desarrollo :rocket:

Para instalar MySQL localmente como si fuera un servidor de bases de datos directamente en tu equipo, debemos hacer distinciones entre sistemas operativos.

Para __MacOS__, deberás instalar un administrador de paquetes llamado [Homebrew](https://brew.sh/index_es), ejecuta el comando que aparece en la pantalla principal para instalar el software.

Una vez instalado, ejecuta los siguientes comandos:

```
  $ brew install mysql
  $ brew tap homebrew/services
  $ brew services start mysql
  $ mysqladmin -u root password 'yourpassword'
```

El último comando es para que modifiques la contraseña de acceso al servidor de bases de datos.

En __Linux__ (basados en Debian, como Ubuntu) basta con ejecutar los siguientes comandos:

```
  $ sudo apt update
  $ sudo apt install mysql-server
```

Para __Windows__, ingresar a la página de descargas de MySQL y elegir el instalador correspondiente https://dev.mysql.com/downloads/windows/installer/, una vez descargado ejecutar el instalador y dejar todas las opciones por defecto. En la lista de aplicaciones a instalar, quitar Workbench pues ya lo hemos instalado.

[`Anterior`](../Readme.md) | [`Siguiente`](../Readme.md)   