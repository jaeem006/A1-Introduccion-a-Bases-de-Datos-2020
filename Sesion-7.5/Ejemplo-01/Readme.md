[`Introducción a Bases de Datos`](../../Readme.md) 

## Ejemplo 1: Llaves foráneas

### 1. Objetivos :dart:
- Relacionar las tablas de una base de datos en SQL definiendo llaves foráneas.


### 2. Requisitos :clipboard:
- Servidor __MySQL__ instalado, puedes usar también los servidores que __BEDU__ ha dispuesto para ti en este módulo.

### 3. Desarrollo :rocket:

1.  Abrir MySQL Workbench 

2. Crear las tabla users con los siguientes comandos de SQL

```sql
   CREATE TABLE users (
   		id INT PRIMARY KEY, 
   		genero VARCHAR(1), 
   		edad INT, 
   		ocup INT, 
   		cp VARCHAR(20)
    );
```
Recordemos que estamos definiendo el campo id como la llave primaria.

3. Crear las tabla movies con los siguientes comandos de SQL

```sql
   CREATE TABLE movies (
   		id INT PRIMARY KEY, 
   		title VARCHAR(100), 
   		genre VARCHAR(100)
    );
```
Recordemos que estamos definiendo el campo id como la llave primaria.

4. Definamos ahora la tabla ratings, si revisamos el archivo README podemos verificar que esta tabla tiene una relación con las otras dos, pues cada valoración está asociado a una película y un usuario. 

Para crear está tabla podría bastar con el siguiente comando
```sql
   CREATE TABLE ratings (
   		userId INT, 
   		movieId INT, 
   		rating INT, 
   		fecha DATETIME
    );
```

Sin embargo esta definición tiene varios detalles, primero no se esta declarando una llave primaria, y esto se debe a que la información por si sola carece de un identificador único o al menos no es tan evidente como en los casos anteriores, segundo no está modelando la relación que existen en las tablas y como se trata de un modelo relacional modelar esto es esencial y por último los valores en userID y movieID podrían ser null lo cual permitiría agregar reseñas de usuarios o películas inexistentes, entonces tenemos que proponer otra solución. 


Primero vamos a definir una llave primaria, para está tabla no tenemos un id como en el caso de las tablas anteriores, así que tenemos 3 opciones para elegir la llave:

- Podemos elegir un campo ya existente como llave primaria, los principales candidatos son userID y movie ID pero en este caso ninguno es único, pues podríamos tener muchas valoraciones sobre la misma película o provenientes del mismo usuario. Por la misma razón los campos rating y fecha no funcionan como llave primaria.

- Agregar un nuevo campo id que sirva como en las tablas anteriores, el problema con esta solución es que ya tenemos un dataset con mas de un millon de registros que tendríamos que modificar agregándoles la llave. Es posible pero es tardado y tedioso.

- Definir una llave primaria compuesta. Las llaves compuestas son formadas por la combinación de dos o mas campos que en conjunto definen un identificador único en este caso podríamos usar la combinación de userId y movieId pues se permite una única valoración de un usuario por película. Para definir la llave primaria compuesta de usa el comando PRIMARY KEY y se indican los campos que conformaran esta llave. Para nuestro ejemplo 
```sql
   CREATE TABLE ratings (
   		userId INT, 
   		movieId INT, 
   		rating INT, 
   		fecha DATETIME,
   		PRIMARY KEY(userId,movieId)
    );
```

Ahora veamos como obligar a que los campos userId y movieId tengan un valor diferente a null. Para esto usamos el comando NOT NULL, este va a obligar a dar valores a estos campos cuando se cree un nuevo registro de esta tabla. Este comando se usa de la siguiente forma:

```sql
   CREATE TABLE ratings (
   		userId INT NOT NULL, 
   		movieId INT NOT NULL, 
   		rating INT, 
   		fecha DATETIME,
   		PRIMARY KEY(userId,movieId)
    );
```

Por último vamos a definir la relación entre las tablas indicando que userId y movieId son llaves foráneas, esto se hace con el comando FOREIGN KEY indicando cual es el campo y después con el comando REFERENCES definimos a que tabla y campo de ésta se está haciendo referencia. 

```sql
    CREATE TABLE ratings (
   		userId INT NOT NULL, 
   		movieId INT NOT NULL, 
   		rating INT, 
   		fecha DATETIME,
   		PRIMARY KEY(userId,movieId),
   		FOREIGN KEY(userId) REFERENCES users(id),
   		FOREIGN KEY(movieId) REFERENCES movies(id)
	);
    );
```

<br/>
  
