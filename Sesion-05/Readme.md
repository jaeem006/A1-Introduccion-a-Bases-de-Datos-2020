[`Introducción a Bases de Datos`](../Readme.md) > `Sesión 5`

## Sesión 5: Fundamentos de MongoDB

<img src="../imagenes/pizarron.png" align="right" height="100" width="100" hspace="10">
<div style="text-align: justify;">

### 1. Objetivos :dart: 
- Configurar una base de datos de __MongoDB__ en la nube.
- Analizar la estructura de distintas colecciones en una base de datos
- Realizar consultas básicas que permitan filtrar documentos, ordenar y limitar los resultados

### 2. Contenido :blue_book:

---

##### <ins>Introducción a __MongoDB__</ins>
<img src="imagenes/imagen.png" align="right" height="300" width="300"> 

MongoDB es un Gestor de Bases de Datos no relacionales orientado a documentos que hace uso de la orientación llave/valor. Su nombre proviene del inglés *humongous* y usa el formato __BSON__ (__JSON__ compilado) para almacenar datos. Es uno de los gestores más conocidos, al mismo nivel que MySQL de las bases de datos relacionales. Algunos conceptos asociados con este tipo de bases son:

- JSON
- Documento
- Colección

```
Tabla -> Colección

Registro -> Documento

Columna -> Llave
```

---

##### <ins>Configuración de __MongoDB__ en la nube</ins>
<img src="imagenes/imagen4.jpg" align="right" height="200" width="300">

Para facilitar la creación de servidores de bases de datos (llamados *clusters* pues se conforman de varios servidores a la vez), __MongoDB__ provee una plataforma que permite crear bases de datos en la nube de forma sencilla. 

Esta plataforma, llamada __Atlas__ permite crear un *cluster* de forma gratuita por lo que lo usaremos para ejemplificar este proceso. Puedes utilizarlo también para tu proyecto.

- [**`EJEMPLO 1`**](Ejemplo-01/Readme.md)

---

##### <ins>Operaciones con bases de datos</ins>
<img src="imagenes/imagen5.png" align="right" height="200" width="300">

Una vez configurado el *cluster* a partir de __MongoDB Atlas__, podemos conectar a la misma a través de __MongoDB Compass__ y por lo tanto podremos crear bases de datos desde aquí.

Lo único que solicita __MongoDB Compass__, a través de una interfaz gráfica, es el nombre de la base de datos.

Por cierto, __MongoDB Compass__ no es el único cliente de __MongoDB__, también existen otras herramientas como __Robo 3T__ o el *shell* de __MongoDB__.

- [**`EJEMPLO 2`**](Ejemplo-02/Readme.md)

---
##### <ins>Realizando operaciones con Colecciones e importando datos</ins>
<img src="imagenes/imagen6.png" align="right" height="100" width="300">

Al igual que en __MySQL__ es posible cargar los datos usando formatos de intercambio de información como son __CSV__ o __JSON__. En el caso de __JSON__ se debe separar cada documento por comas.

- [**`EJEMPLO 3`**](Ejemplo-03/Readme.md)
- [**`RETO 1`**](Reto-01/Readme.md)

---


#### <ins>Colecciones, Documentos y Proyecciones</ins>
<img src="imagenes/imagen2.jpg" align="right" height="200" width="300">

En __MongoDB__ los datos son almacenados en *colecciones* que incluyen documentos. Estos documentos se representan usando el formato de intercambio de información __JSON__. El formato __JSON__ se conforma de un conjunto de elementos de la forma *clave-valor* separados por comas y delmitados por llaves. Los tipos de datos de __JSON__ son:

- Números
- Booleanos
- Cadenas
- Arreglos
- Objetos

Para realizar consultas u otras operaciones en __MongoDB__ debe usarse este formato a manera de lenguaje (no es un lenguaje por sí mismo, pero lo usaremos como si lo fuera). En particular, para realizar proyecciones, se usa este formato. Debe indicarse el campo a proyectar y colocar un uno si queremos mostrarlo o cero en caso contrario.

- `{campo: 0}`
- `{campo: 1}`

- [**`EJEMPLO 4`**](Ejemplo-04/Readme.md)
- [**`RETO 2`**](Reto-02/Readme.md)	

---
#### <ins>Filtros básicos</ins>
<img src="imagenes/imagen3.png" align="right" height="200" width="300">

Al igual que con las proyecciones, los filtros se construyen usando __JSON__. En su forma más básica se debe escribir el nombre del campo, dos puntos y el valor que queremos filtrar. Existen varias funciones que se pueden combinar con los filtros y las iremos estudiando a lo largo del módulo.

```json
{campo: "valor"}
```

- [**`EJEMPLO 5`**](Ejemplo-05/Readme.md)
- [**`RETO 3`**](Reto-03/Readme.md)

---

### 3. Ejercicios para practicar :hammer:

Aplica lo todo lo que aprendiste durante la sesión en esta serie de ejercicios. 

- [**`Ejercicios Sesión 5`**](Ejercicios/Readme.md)

### 4. Postwork :memo:
Aplica lo todo lo que aprendiste durante la sesión a tu proyecto personal.

- [**`POSTWORK SESIÓN 5`**](Postwork/Readme.md)

</br>

[`Anterior`](../Sesion-04/Readme.md) | [`Siguiente`](../Sesion-06/Readme.md)

</div>	
