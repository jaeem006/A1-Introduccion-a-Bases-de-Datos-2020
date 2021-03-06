[`Introducción a Bases de Datos`](../../Readme.md) > [`Sesión 01`](../Readme.md) > `Ejemplo 1`

## Ejemplo 1: Conexión a bases de datos

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Realizar la conexión a una base de datos mediante un cliente.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado o un cliente para MySQL

### 3. Desarrollo :rocket:

## Utilizando Workbench

1. Abre MySQL Wokbench. En esta primera pantalla se muestran las conexiones que tienes configuradas o se muestra en blanco en caso de que sea la primera vez que realizas una conexión.

   ![imagen](imagenes/s1-w1.png)

2. Junto al título `MySQL Connections` da clic en el botón de más. Se abrirá una nueva ventana solicitando los datos para realizar la conexión correspondiente. Introduce los datos necesarios para realizar la conexión. Pide al experto que te los proporcione.

   - **Connection Name:** Un nombre de tu preferencia para recordar a qué servidor te estás conectando.
   - **Hostname:** Dirección del servidor al cuál nos conectaremos.
   - **Port:** Puerto a través del cual realizaremos la conexión.
   - **Password:** Contraseña de acceso. Da clic en el botón `Store in Keychain ...` e introduce la contraseña.
   
   ![imagen](imagenes/s1-w2.png)

3. Presiona el botón `Test Connection` y si obtienes un mensaje como el que se muestra en la siguiente imagen, entonces los datos de la conexión son correctos y presiona el botón `Ok`. En caso contrario revisa las credenciales.

   ![imagen](imagenes/s1-w3.png)

4. Se añadirá la conexión que acabas de configurar a la pantalla inicial.

   ![imagen](imagenes/s1-w4.png)

5. Da clic sobre la conexión que se agregó a la pantalla inicial, se mostrará una ventana como la de la imagen.

   ![imagen](imagenes/s1-w5.png)

## Utilizando un cliente en la terminal

Como alternativa a los clientes con interfaz gráfica MySQL tiene también clientes que corren en la terminal, la ventaja de estos es que son mas eficientes, es decir consumen menos tiempo en ejecutar los comando.

Uno de los clientes de MySQL para la terminal es **mycli** que es un cliente desarrollado en Python y corre en el entorno de desarrollo para este lenguaje **anaconda**. 

Para instalarlo puedes consultar el siguiente [enlace](https://www.mycli.net/install).

Una vez instalado podemos conectarnos al servidor de base de datos con el siguiente comando desde la terminal.

```bash
mycli -h <host> -u <usuario> -p <contraseña> -P <puerto>
```

Por ejemplo

```bash
mycli -h ec2-34-220-57-78.us-west-2.compute.amazonaws.com -u root -p *9ak/oVTwtY_eI:. -P 3306
``` 

Dentro de este cliente los comandos de SQL son los mismos que en Workbench, lo único que cambia es la presentación de los resultados.

**¡Felicidades! Haz realizado tu primera conexión a una base de datos**

[`Anterior`](../Readme.md#bases-de-datos-relacionales) | [`Siguiente`](../Readme.md#estructura-de-una-tabla)

</div>
