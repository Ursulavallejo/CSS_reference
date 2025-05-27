##information reference:


[Crear un carrusel de imágenes solo con CSS ](https://www.enmilocalfunciona.io/crear-un-carrusel-de-imagenes-solo-con-css/)

#Notes:


#CSS Scroll Snap:

-"slider" o carrusel de elementos: usando  CSS Scroll Snap.

-Este Scroll Snap te va a permitir generar puntos de ajuste para el inicio, centro y final de los elementos, y así poder generar el efecto de carrusel.



###Propiedad CSS scroll-snap-type:

scroll-snap-type, esta se aplica en nuestro contenedor donde vamos a querer controlar el scroll. Vamos a tener que indicarle dos parámetros:

El primero sería si queremos controlar el scroll en una dirección u otra.

none: Cuando se hace scroll en el contenedor, se ignoran los puntos de ajuste.
x: Puntos de ajuste son horizontales.
y: Puntos de ajuste son verticales.
both: Puntos de ajuste son tanto horizontales como verticales.
El segundo parámetro determina si el viewport de nuestro contenido se debe ajustar a los elementos de forma obligatoria o solo si está muy próximo de sus bordes.

mandatory: Al terminar de hacer scroll, el scroll se mueve automáticamente SIEMPRE al punto de ajuste que se haya determinado.
proximity: Al terminar de hacer scroll, el scroll se mueve automáticamente SOLO cuando el scroll esté muy próximo al punto de ajuste que se haya determinado.

```
.slider-container {
scroll-snap-type: x mandatory;
}
```

###Propiedad CSS scroll-snap-type:

-scroll-snap-align, esta propiedad se usa en cada uno de los elementos que tenemos en nuestro contenedor donde vamos a indicarle como va a alinearse este elemento en el viewport.

-El primer parámetro se refiere x, es decir, izquierda y derecha. Y el segundo se refiere a y, es decir, arriba y abajo (Funciona de manera similar a margin o padding). Si usamos un solo parámetro, este se referirá a todas las direcciones. Los parámetros aceptados son los siguientes:

none: El elemento no tiene ningún punto de ajuste en su eje.
start: El elemento tiene como punto de ajuste su inicio.
end: El elemento tiene como punto de ajuste su final.
center: El elemento tiene como punto de ajuste su centro.

```
.slider-container img {
  scroll-snap-align: center;
}
```

###Ejemplo práctico

``` HTML
<div class="slider-container">  
  <img
    class="slider-item"
    src="https://images.unsplash.com/photo-1580501170961-bb0dbf63a6df?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2970&q=80"
  />
  <img
    class="slider-item"
    src="https://images.unsplash.com/photo-1580501170888-80668882ca0c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80"
  />
  <img
    class="slider-item"
    src="https://images.unsplash.com/photo-1572508589584-94d778209dd9?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80"
  />
</div>  
}
```

``` CSS
.slider-container {
  display: flex;
  width: 100%;
  height: 100vh;
  overflow-x: scroll;
}

.slider-container img {
  flex: 0 0 100%;
  width: 100%;
  object-fit: cover;
}
```
CSS>
Con esto conseguiremos que las imágenes estén alineadas de izquierda a derecha. Para ello usaremos: 

display: flex 

en nuestro contenedor para que se alineen todos los elementos hijo. Además, vamos a decirle que 

ocupe el 100% de la pantalla usando el width: 100% y height: 100vh.

En el caso de las imágenes vamos a estirarlas usando:

flex: 0 0 100% y width: 100% 

para que estas ocupen el 100% del contenedor, y para que no nos queden con una relación de aspecto erróneo usaremos: 

object-fit: cover.

``` agregar scroll-nap CSS
.slider-container {
  display: flex;
  width: 100%;
  height: 100vh;
  overflow-x: scroll

  /* Vamos a añadir esto 👇 */
  scroll-snap-type: x mandatory;
}

.slider-container img {
  flex: 0 0 100%;
  width: 100%;
  object-fit: cover;

  /* Vamos a añadir esto 👇 */
  scroll-snap-align: center;
}
```

Usaremos en el contenedor la propiedad scroll-snap-type: x mandatory;. 

Esto nos indicará que queremos capturar el scroll horizontal del contenedor y que es obligatorio que siempre, al dejar de hacer scroll, vaya a un punto de anclaje. De esta forma evitaremos que nuestro carrusel se quede en mitad de dos imágenes.

Y en las imágenes, usaremos la propiedad scroll-snap-align: center;. 

Esto le indicará que el punto de anclaje es el centro del elemento. Así, nuestras imágenes siempre quedarán alineadas.

Nota importante a tener en cuenta: 
Hay que usar este overflow-x: scroll en el contenedor de nuestro carrusel, ya que si no estaríamos haciendo scroll sobre el elemento <body> y no estamos capturando el scroll del elemento .slider.



[//]: # ([<img src="./imgDoku/user-api.png" width="250"/>]&#40;./imgDoku/user-api.png&#41;)