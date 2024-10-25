* Nombre: Matias Casiba
* Link Github Repo:
* Link Netlify:

# Páginas de restaurantes
Para armar esta página, utilizaremos los siguientes elementos en el index.html:
```sh
<h1> Título </h1>
<img src="dirección-imagen" alt="nombre de la imagen"> # para las imágenes
```
## Agregando colores y fuente
Para nuestro fondo usaremos en css: 
```sh
body{
  background-color: rgb(56, 185, 172);
}
```
### Fuente del título y color
En el elemento h1, le daremos color al título, una tipografía y tamaño con css:
```sh
h1{
  color: rgb(217, 255, 27); #color del título
  font-size: 40px; # tamaño del título
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif; # tipografía
  text-align: center; # centra el título
}
```

## Diseño de imágenes y borde
Para modificar las imágenes, estaré trabajando con su alto, dejando su ancho en automático, le agrgaré un borde y espacios entre las imágenes
```sh
img{
  width: auto; # ancho
  height: 120px; # alto
  border: 10px solid white; # grosor, estilo y color
  margin: 5px 5px 5px 5px; # margen (5px) arriba(5px), derecha(5px), abajo(5px) y izquierda(5px)
}
```

Si quiero que las imágenes se ubiquen de manera horizontal, que cuando termine el margen se coloque debajo las demás imágenes y sigan yendo horizontalmente, trabajaré con un elemento div en el archivo index.html. Dentro de ese div anidaré los elementos imágenes, ¿por qué? porque al div le agregaré una clase para poder modificar en css, esto me vitaría de estar agregando a cada elemento img (elemento de imagen) una clase. Osea que la clase en el div lo heredarán los elementos img:
```sh
<div class="image-centrada">
    # los 10 elementos <img>
</div>
```

Ahora en css agregaré lo siguiente:
```sh 
img{
  display: inline-block; # su función es hacer que las imágenes se comporten como bloques en línea
}

.image-centrada{
  text-align: center; # centrará las imágenes
  white-space: normal; # permite que las imágenes pasen a la siguiente línea
}
```
* Nota: el white-space, va a lograr que los elementos inline-block pasen a la siguiente línea cuando no haya espacio en una fila. Podría decir que no sería necesario agregar esto, pero correría el riesgo de que no funcione correctamente como quiero, osea que las imágenes no podrían saltar a la siguiente línea de manera correcta.
* Explicando más de como funciona el display: inline-block, hace que las imágenes se comporten como elementos inline, pero mantiene las propiedades de bloque, como el ajuste de su ancho, alto y otras cosas. Esto ahora me va a permitir que las imágenes vayan de forma horizontal. 
* El text align me asegura de que las imagenes se centren dentro del contenedor div.