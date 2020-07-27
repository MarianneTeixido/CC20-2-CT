# JavaScript

## Diferencias entre Processing y P5js

### Display 

En lo general Processing y P5 son muy parecidos. Pero tienen diferencias que es importante tener presente antes de empezar a codear en _pifive_.

Debido a que la web nos permite pensar y hacer más allá de las resticciones del sketch que funjía como lienzo para el dibujo, en P5 size() ha sido reemplazado por createCanvas().

### Rate

frameRate(num) establece la velocidad de fotogramas pero la variable frameRate ha sido eliminada. Para obtener la velocidad de fotogramas hay que llamar a frameRate() sin argumentos. 

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

### Transformaciones

pushMatrix() y popMatrix() se han reemplazado por push() y pop(), el equivalente a invocar juntos los métodos de matriz y de estilo.

Por defecto, todo está en el espacio de nombres global, y podemos crear sus bocetos como lo hace con el procesamiento. Sin embargo, hay algo que llamamos "modo de instancia" para crear un boceto p5 que funciona bien con el resto del código que se ejecuta en su página. Vea este ejemplo de modo de instancia y este tutorial de modo de instancia global vs.

### Imprimir información

La función println () no está disponible en p5.js. Por lo que debemos usar print () o console.log ().

### Coordenadas en 3D

El origen (0, 0, 0) para el modo WEBGL está en el centro del canvas, en lugar de en la parte superior izquierda, ya que está en modo 2D.

WebGL utiliza matrices de columnas principales. Al traducir bocetos 3D que aplican matrices de Processing a p5, las matrices se pueden transponer para lograr los mismos resultados.

### Nota

No todo en Processing se implementa en p5.js, pero es un proyecto que se encuentra en constante desarrollo. Por ejemplo, hasta la última actualización aún no había un equivalente a la librería PShape. La cámara en p5js es todavía muy básica, cuanta sólo con la posición del ojo pero no tienen _lookat_ o _axis direction_.

Para conocer el estado actual de una función o librería lo mejor es siempre consultar la [documentación](https://p5js.org/es/reference/), para saber cuáles funcionan y cuáles no. 

## Sobre JavaScrip 

- Las variables no tienen un tipo de dato. Debemos de usar _let_ (o en la sintaxis anterior _var_) en lugar de float, int, char, String, Array, etc. 



## Referencias

[Overview of differences](https://github.com/processing/p5.js/wiki/Processing-transition)
