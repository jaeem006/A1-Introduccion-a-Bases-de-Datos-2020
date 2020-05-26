[`Introducción a Bases de Datos`](../../Readme.md) 

## Ejemplo 1: Creación de JSON

### 1. Objetivos :dart:
- Repasar el concepto de JSON
- Conocer los tipos de dato que se pueden almacenar en un JSON
- Crear archivos JSON


### 2. Requisitos :clipboard:
- Un editor de texto

### 3. Desarrollo :rocket:

1.  Los principales usos del formato JSON son:

- Transmitir información estructurada y ligera a través de una red, principalmente internet.
- Las API's utilizan este formato para proveer información.
- Se usan como estructuras de datos en lenguajes de programación modernos.
- Se utilizan para modelar bases de datos NoSQL (no relacionales).

2. Veamos cual es la sintaxis para definir un JSON, está es un subconjunto de la sintaxis de JavaScript.
- La información se representa con pares nombre/valor.
- Los Objetos son delimitados pos llaves { }.
- Primero se escribe el nombre y seguido de dos puntos : después va el valor.
- Los elementos están separados por una coma.
- Los arreglos son delimitados por corchetes, los elementos de estos también se separan por comas.

Veamos un ejemplo sencillo:

```json
{
   "book": [

      {
         "id": "01",
         "language": "Java",
         "edition": "third",
         "author": "Herbert Schildt"
      },

      {
         "id": "07",
         "language": "C++",
         "edition": "second",
         "author": "E.Balagurusamy"
      }

   ]
}
```

<br/>
  
