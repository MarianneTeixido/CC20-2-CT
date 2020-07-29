# JavaScript y P5

## Diferencias entre Processing y P5js


En lo general Processing y P5 son muy parecidos. Pero tienen diferencias que es importante tener presente antes de empezar a codear en P5.

### Funciones 

El bloque de código que antes se llamaba _void_ setup() y _void_ draw() ahora se llama _function_ setup() y _function_ draw(), los cuales se comportan exactamente igual que void. Como ahora estamos usando algunas librerías de JavaScript esos bloques de código heredan la sintaxis de este lenguaje. 

### Display 

Debido a que la web nos permite pensar y hacer más allá de las resticciones del sketch que funjía como lienzo para el dibujo, en P5 size() ha sido reemplazado por createCanvas().

## Tipos de datos 

- Las variables no tienen un tipo de dato. Debemos de usar _let_ (o en la sintaxis anterior _var_) en lugar de float, int, char, String, Array, etc. 

### Sincronía

JavaScript no siempre carga las cosas sincrónicamente, por lo que hay un par de opciones para lidiar con esto:

- Usar _callback_. Es decir, una función que se llama después de cargar el archivo.
- Alternativamente, podemos usar el método preload () que ocurre antes de setup (). Si existe el método preload(), la configuración esperará hasta que se cargue todo el contenido, como se ve en [este ejemplo](https://p5js.org/es/examples/image-alpha-mask.html).

### Interacción con el mouse

La variable mousePressed ha sido reemplazada por mouseIsPressed.

Además de los eventos del mouse, hay eventos _touch_. El mapeo es así:

- mouseX ~ touchX
- mouseY ~ touchY
- mousePressed () ~ touchStarted ()
- mouseDragged () ~ touchMoved ()
- mouseReleased () ~ touchEnded ()

Hay una matriz de _touches_ [] que contiene una serie de objetos con propiedades x, y correspondientes a la posición de cada dedo.

Touch está diseñado para la interacción con dispositivos móviles como teléfonos celulares y tabletas, con lo cual podemos diseñar aplicaciones que corran en este tipo de dispositivos. 

### Transformaciones

pushMatrix() y popMatrix() se han reemplazado por push() y pop() 

### Imprimir mensajes en la consola

La función println () no está disponible en p5.js. Por lo que debemos usar print () o console.log (). Este último método es el mismo que se usa en JavaScript.

### Coordenadas en 3D

El origen (0, 0, 0) para el modo WEBGL está en el centro del canvas, en lugar de en la parte superior izquierda.

### NOTA

No todo en Processing se implementa en p5.js, pero es un proyecto que se encuentra en constante desarrollo. Por ejemplo, hasta la última actualización aún no había un equivalente a la librería PShape. La cámara en p5js es todavía muy básica, cuenta sólo con la posición de la cámara pero no tiene _lookat_ o _axis direction_.

Para conocer el estado actual de una función o librería lo mejor es siempre consultar la [documentación](https://p5js.org/es/reference/), para saber cuáles funcionan y cuáles no. 

## Ejemplos de traducción 

Este es el setup básico de un sketck en Processing y p5.js 

```java
void setup() {
  // elementos del setup 
}

void draw() {
  // elementos del draw 
}
```

```javascript
function setup() {
  // elementos del setup 
}

function draw() {
  // elementos del draw
}
```


### Convertir un sketck de Processing a p5.js

Abajo tenemos un ejemplo de un sketch convertido de Processing a p5.js Los cambios se muestran en los comentarios. 

```javascript
/**
 * Este ejemplo lo pueden encontrar en los ejemplos de Processing
 * al cual pueden acceder desde el IDE de Processing
 * Processing > Examples > Basics > Form > Bezier
 * Adaptado por Evelyn Eastmond
 */

function setup() {           // **cambió** void setup() a function setup()
  createCanvas(640, 360);    // **cambió** size() a createCanvas()
  stroke(255);               // stroke() es el mismo
  noFill();                  // noFill() es el mismo
}

function draw() {                         // **cambió** void draw() a function draw()
  background(0);                          // background() es el mismo
  for (var i = 0; i < 200; i += 20) {     // **cambió** int i a var i
    bezier(mouseX-(i/2.0), 40+i, 410, 20, 440, 300, 240-(i/16.0), 300+(i/8.0)); // bezier() es el mismo.
  }
}
```

### Declarar variables

En p5 todas las variables (no importa si son número, strings, arrays, funciones, objetos o lo que sea) son declaradas usandoo el símbolo var (o en nuevas versiones de navegadores, let or const). A diferencia de Processing, no tenemos que especificar el tipo de variable. 

Por ejemplo, si tenemos: 

```java
boolean boton = false;
```
nosotros debemos de escribir

```javascript
var boton = false;
```
o en lugar de: 

```java 
float x = 100.3;
```
nosotros debemos de escribir 

```javascript
var x =  100.3;
```


### Ejercicio 1

Adapatar un sketch de la documentación [Learning Processing de Daniel Shiffman](https://github.com/shiffman/LearningProcessing) y trasladarlos a p5.js en el [editor de P5](https://editor.p5js.org/).





## Referencias

[Overview of differences](https://github.com/processing/p5.js/wiki/Processing-transition)
