
# Clase 1 | Internet y desarrollo web (Repaso)

## ¿Cómo funciona internet?

![portada2](https://github.com/MarianneTeixido/CC20-2-CT/blob/master/img/internet.png)

[_Hello World_, Taeyoon Choi, 2017.](http://avant.org/project/hello-world/)

Internet trabaja mediante paquetes de ruteo de redes de acuerdo a _Internet Protocol (IP)_, _Transport Control Protocol (TCP)_, entre otros. 

Un protocolo es una serie de reglas que especifican cómo las computadoras deben de comunicarse entre ellas en una red.  
Por ejemplo, el TCP tiene la regla de que si una computadora manda datos a otra computadora, la computadora de destino debe dejar que la computadora fuente sepa si algún dato se perdió o si la computadora fuente debe reenviarlo. O el IP que especifica cómo las computadoras deben de rutear la información a otra, adjuntando direcciones en los datos que se envían.  


Antecedentes: El intenet comenzó con ARPANET en los 60 con el objetivo de tener una red de computadoras descentralizada. 

Para optener la IP de un dispositivo, se tendría que saber la dirección del servidor que provee los servicios de Internet. 

## Aplicaciones cliente - sevidor 

![server-client](https://github.com/MarianneTeixido/CC20-2-CT/blob/master/img/cliente-servidor.png)

El servidor es un ordenador en donde se ejecuta un programa que realiza tareas que benefician a los dispositivos cliente. Los servidores realizan procesamientos que gestionan el tráfico en la red a los clientes como el acceso a internet, correo electrónico entre otros. 

Otros tipos de arquitectura, [ventajas y desventajas de las aplicaciones cliente servidor](https://es.wikipedia.org/wiki/Cliente-servidor). 

DigitalOcean. 


## Introducción a HTML

![html](https://github.com/MarianneTeixido/CC20-2-CT/blob/master/img/html.png)

[Lenguaje de Marcado de Hipertextos](https://developer.mozilla.org/es/docs/Web/HTML) (_HyperText Markup Languaje_), es el elemento más básico para la construcción de la web. Se usa para dar sentido y estructura del contenido a la página web. Otras tecnologías, además del HTML, que son usadas para describir la apariencia de una página web son CSS y JavaScript. 

### Modelos DOM y CSS

Los modelos [DOM](https://www.digitalocean.com/community/tutorials/introduction-to-the-dom) (_Document Object Model_ o Modelo de Objetos de Documento) es una parte escencial para la interactividad en la web. Es una interfaz que permite al lenguaje de programación manipular el contenido, estructura y el estilo de la página web.  

Con el Modelo de Objetos del Documento los programadores pueden construir documentos, navegar por su estructura, y añadir, modificar o eliminar elementos y contenido". Es decir que tiene una escructura flexible en la cual se pueden añadir o quitar elementos  

En el DOM los documentos tienen una estructura parecida a un arbol, creando una estructura jerarquica en la que de un objeto principal pueden depender varios secundarios. Esto se ve claramente en la escructura que tiene la página de HTML, la cual consta de etiquetas anidadas.

Por ejemplo si tenemos una página web sencilla:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Mi página</title>
</head>
<body>
  <h1>Hola mundo</h1>
	<p>Esta es mi página.</p>
</body>
</html>
```

Prueba pegando ese código en este editor dando click [aquí](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_default)

![dom-arbol](https://github.com/MarianneTeixido/CC20-2-CT/blob/master/img/dom.gif)

Cada recuadro es un nodo, los nodos son la estructura más básica de una DOM. Estos nodos son jerárquicos y están interrelacionados. DOM define 

- Elementos como objetos en HTML
- Propiedades de todos los elementos HTML
- Métodos para acceder a todos los elementos del HTML
- Eventos para todos los elementos HTML  

En su forma más básica HTML es el nivel más básico de programación web. El navegador que usamos para ver el sitio web es un programa que interpreta HTML y CSS y representa el estilo, el contenido y la estructura en la página web. 

CSS (_Cascading Style Sheets_ o Hojas de estilo en cascada) es un código complementa el HTML y permite configurar características visuales como forma color y posición en una página. 

DOM de CSS permite que JavaScript acceda al contenido de texto y elementos del documento del sitio web como objetos. 

[Ejercicio] (https://www.vice.com/es_latam): Modificar el atributo de algun objeto DOM, como texto.

![dom2-arbol](https://github.com/MarianneTeixido/CC20-2-CT/blob/master/img/dom2.gif)

Ejercicio 2: Abrir el navehador de google y cambiar el estilo de color.
- Escribir en la consola.
 
```html
document.body.style.backgroundColor = 'fuchsia';
```

El código JavaScript que escribimos, asignando fucsia al color de fondo del cuerpo, ahora es parte del DOM.


## JavaScript 

Javascript es una forma de complementar una página web, mediante aplicaciones dinámicas. Las páginas Web que podemos hacer usando sólo los lenguajes HTML y CSS son páginas estáticas; es decir, podemos poner texto, imágenes, colores, etc. pero el usuario lo único que puede hacer es verlas, leerlas, ir a otra página con los enlaces, o como mucho rellenar un formulario.

Con javascript cambia el concepto de la página. Podemos hacer la página más interactiva, de forma que tanto el programador como el usuario puedan realizar más acciones dentro de la página.

Algunas de las cosas que podemos realizar con Javascript:

- Dar mensajes de alerta.
- Incluir botones para mostrar u ocultar elementos.
- Incluir botones para cambiar colores, estilos, etc de los elementos.
- Incluir un reloj o cronómetro en la página.
- Incluir calculadoras o tablas de cálculo.
- Mostrar ventanas emergentes.
- Dar movimiento a algunos elementos de la página.
- Comprobar los datos de un formulario antes de enviarlo.

¿Páginas que usen javascript?

## Distribución de la imagen en movimiento 

Debate. 





