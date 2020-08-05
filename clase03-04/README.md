# Estructuras de datos en JS

## Archivos JSON

JavaScript Object Notation (JSON) es un formato basado en texto estándar para representar datos estructurados en la sintaxis de objetos de JavaScript. Es comúnmente utilizado para transmitir datos en aplicaciones web (por ejemplo: enviar algunos datos desde el servidor al cliente, así estos datos pueden ser mostrados en páginas web, o vice versa). 

Este archivo fue popularizado por Douglas Crockford. Aunque este tipo de archivo es usado bajo la sintaxis de JavaScript, es posible _parsearlo_ para que pueda ser leído por otros lenguajes, además de que muchos entornos de programación ya poseen la capacidad de leer y generar JSON. 

Nota: Convertir una cadena a un objeto nativo se denomina _parsing_.

Un objeto JSON puede ser almacenado en su propio archivo, que es básicamente sólo un archivo de texto con una extension .json

## Estructura de un JSON

Un JSON es una cadena cuyo formato es similar al de los objetos literales JavaScript. Es posible incluir los mismos tipos de datos básicos dentro de un JSON que en un objeto estándar de JavaScript - cadenas, números, arreglos, booleanos, y otros literales de objeto. Esto permite construir una jerarquía de datos, como ésta:

```javascript
{
  "squadName": "Super hero squad",
  "homeTown": "Metro City",
  "formed": 2016,
  "secretBase": "Super tower",
  "active": true,
  "members": [
    {
      "name": "Molecule Man",
      "age": 29,
      "secretIdentity": "Dan Jukes",
      "powers": [
        "Radiation resistance",
        "Turning tiny",
        "Radiation blast"
      ]
    },
    {
      "name": "Madame Uppercut",
      "age": 39,
      "secretIdentity": "Jane Wilson",
      "powers": [
        "Million tonne punch",
        "Damage resistance",
        "Superhuman reflexes"
      ]
    },
    {
      "name": "Eternal Flame",
      "age": 1000000,
      "secretIdentity": "Unknown",
      "powers": [
        "Immortality",
        "Heat Immunity",
        "Inferno",
        "Teleportation",
        "Interdimensional travel"
      ]
    }
  ]
}
```

Para acceder a los datos que se encuentran más abajo en la jerarquía, simplemente se debe concatenar los nombres de las propiedades y los índices de arreglo requeridos. Por ejemplo, para acceder al tercer superpoder del segundo héroe registrado en la lista de miembros, se debería hacer esto: 

```javascript
superHeroes['members'][1]['powers'][2]
```

- Primero el nombre de la variable — superHeroes.
- Dentro de esta variable para acceder a la propiedad members utilizamos ["members"].
- members contiene un arreglo poblado por objetos. Para acceder al segundo objeto dentro de este arreglo se utiliza [1].
- Dentro de este objeto, para acceder a la propiedad powers utilizamos ["powers"].
- Dentro de la propiedad powers existe un arreglo que contiene los superpoderes del héroe seleccionado. Para acceder al tercer superpoder se utiliza [2].

## Arreglos como JSON

Anteriormente mencionamos que el texto JSON básicamente se parece a un objeto JavaScript. La razón de esto es que un arreglo es también un JSON válido, por ejemplo:

```javascript
[
  {
    "name": "Molecule Man",
    "age": 29,
    "secretIdentity": "Dan Jukes",
    "powers": [
      "Radiation resistance",
      "Turning tiny",
      "Radiation blast"
    ]
  },
  {
    "name": "Madame Uppercut",
    "age": 39,
    "secretIdentity": "Jane Wilson",
    "powers": [
      "Million tonne punch",
      "Damage resistance",
      "Superhuman reflexes"
    ]
  }
]
```

![json-ejemplo](https://github.com/MarianneTeixido/CC20-2-CT/blob/master/img/json-superheroes.png)

### Notas

- JSON es sólo un formato de datos — contiene sólo propiedades, no métodos.
- JSON requiere usar comillas dobles para las cadenas y los nombres de propiedades. Las comillas simples no son válidas.
- Una coma o dos puntos mal ubicados pueden producir que un archivo JSON no funcione. Se debe ser cuidadoso para validar cualquier dato que se quiera utilizar (aunque los JSON generados por computador tienen menos probabilidades de tener errores, mientras el programa generador trabaje adecuadamente). Es posible validar JSON utilizando una aplicación como JSONLint.
- JSON puede tomar la forma de cualquier tipo de datos que sea válido para ser incluido en un JSON, no sólo arreglos u objetos. Así, por ejemplo, una cadena o un número único podrían ser objetos JSON válidos.
- A diferencia del código JavaScript en que las propiedades del objeto pueden no estar entre comillas, en JSON, sólo las cadenas entre comillas pueden ser utilizadas como propiedades-

## API

Las API (_Application Programming Interface_ o Interfaz de Programación de Aplicaciones) son un conjunto de funciones, procedimientos y protocolos que cumplen una o muchas funciones con el fin de ser utilizadas por otro software. Una API permite implementar funciones y procedimientos dentro de nuestro proyecto sin la necesidad de programarlas de nuevo. En términos de programación, es una capa más de abstracción. 

Las API permiten la comunicación entre dos aplicaciones de software a través de un conjunto de reglas. Esta comunicación depende del fin y los permisos que otorguen los propietarios de la API para los desarrolladores de terceros. 


Al usar una API todo el desarrollo que se quiera realizar estará limitado por los métodos o funciones que esta incluya, es decir, no pueden ser añadidas nuevas funcionalidades. De esta manera compañías como Twitter se aseguran de lo que pueden o no hacer los clientes desarrollados por terceros.

Tweetbot, Birdie, Turpial, Fenix, Carbon, Metrotwit, Tweepy; todos son clientes de Twitter diferentes pero construidos usando la misma base, la API de Twitter.


## API - JSON

Mediante es uso de API es posible hacer peticiones para acceder a archivos JSON. Este métido nos hace más accesible la información para el desarrollo web de nuestros proyectos.









