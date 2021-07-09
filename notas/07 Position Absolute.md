# Position Static

Los elementos de posición estática no se ven afectados por las propiedades superior, inferior, izquierda y derecha. 

Un elemento con `position: static;` no se posiciona de ninguna manera especial; siempre se posiciona de acuerdo con el flujo normal de la página:

# Position Relative

Un elemento con `position: relative;` está posicionado en relación con su posición normal.

Establecer las propiedades superior, derecha, inferior e izquierda de un elemento en una posición relativa hará que se ajuste lejos de su posición normal. El resto del contenido **no se ajustará** para encajar en ningún espacio dejado por el elemento.

# Position Fixed

Un elemento con `position: fixed;`está posicionado en relación con la ventana gráfica, lo que significa que siempre permanece en el mismo lugar incluso si se desplaza la página. Las propiedades superior, derecha, inferior e izquierda se utilizan para colocar el elemento. 

![Screenshot_20210422_123357.png](/home/genaro_javier/Imágenes/Screenshot_20210422_123357.png)

![Screenshot_20210422_123439.png](/home/genaro_javier/Imágenes/Screenshot_20210422_123439.png)

# Position Absolute

Un elemento con `position: absolute;`está posicionado en relación con el antepasado posicionado más cercano (en lugar de posicionado en relación con la ventana gráfica, como el fixed).

Su funcionamiento es similar al position relative, pero al contrario que el relative, el obsolute no guarda un espacio reservado lo que hace pensar que la imagen desapareció. 

**Cuando usamos esta propiedad, el ancho de cualquier elemento se va a ajustar automáticamente al contenedor.**

# Propiedades

- **Opacity** Esta propiedad hace que el elemento sea transparente y toma valores de entre 1 y 0 donde 1 es totalmente opaco y 0 totalmente trasparente. 

# Código

```html
<!DOCTYPE html>
<html>
<head>
    <title>Propiedades de Texto</title>
    <link rel="stylesheet" type="text/css" href="css/estilos2.css">
    <link rel="stylesheet" type="text/css" href="css/normalize.css">
    <!--Fuentes-->
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Abril+Fatface&display=swap" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Hind+Madurai:wght@300&display=swap" rel="stylesheet">
</head>

<body>
    <div class="contenedor">
        <div class="caja1"><h1>Caja 1</h1></div>
        <div class="caja2"><h1>Caja 2</h1></div>
        <div class="caja3"><h1>Caja 3</h1></div>
        <div class="caja4"><h1>Caja 4</h1></div>
        <div class="caja5"><h1>Caja 5</h1></div>
    </div>
</body>
</html>
```

```css
* {
    font-family: 'Abril Fatface', cursive;
    font-size: 10px; 
    font-weight: 100; 
}

div {
    display: block;
    background: yellow; 
}

/*Asi podemos aplicar estilos a los div que estan
dentro de otros div*/
div div {
    background: yellow; 
    width: 100px; 
    height: 100px;
    position: absolute;
    border: 1px solid blue; 
}

.contenedor {
    position: relative;
    border: 4px solid red; 
    margin: 50px auto; 
    background: green; 
    width: 500px; 
    height: 500px; 
}

.caja1 {
    left: 0; 
    top: 0; 

}
.caja2 {
    right: 0; 
    top: 0; 
}

.caja3 {
    bottom: 0; 
    left: 0; 
}

.caja4{    
    bottom: 0;
    right: 0; 
}

.caja5{    
    /*Asi podemos centrar un elemento, en el caso de
    no conocer sus medidas*/
    top: 0; 
    bottom: 0; 
    left: 0; 
    right: 0;
    margin: auto;
}
```

![Screenshot_20210422_092641.png](/home/genaro_javier/Imágenes/Screenshot_20210422_092641.png)

# Position Sticky

Un elemento con `position: sticky;`se posiciona según la posición de desplazamiento del usuario.

Un elemento fijo alterna entre `relative`y `fixed`, según la posición de desplazamiento. Se coloca en una posición relativa hasta que se alcanza una posición de desplazamiento determinada en la ventana gráfica, luego se "pega" en su lugar (como posición: fija).

![Screenshot_20210422_124005.png](/home/genaro_javier/Imágenes/Screenshot_20210422_124005.png)

![Screenshot_20210422_123934.png](/home/genaro_javier/Imágenes/Screenshot_20210422_123934.png)

# Notas

- El **Viewport** es todo lo que vemos en el navegador (El espacio en blanco)
