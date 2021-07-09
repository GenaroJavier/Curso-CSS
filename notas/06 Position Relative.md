# Relative Position

Posiciona los elementos, al utilizar esta propiedad adquirimos otras 5 las cuales son: top, bottom, rigth ,left, el Z-indez y los tipos de posición son los siguientes: 

- **Static** Cuando se pone esta propiedad es como si nosotros especificáramos que no esta posicionado. 

- **Relative** Cuando posicionamos un elemento de forma relative, pareciera que no cambia nada pero no es así, con esta propiedad decimos que queremos que siga conservando su espacio esto quiere decir que, tenemos las siguientes 4 cajas. 
  
  <img src="file:///home/genaro_javier/Imágenes/Screenshot_20210403_115252.png" title="" alt="Screenshot_20210403_115252.png" data-align="center">
  
  ```css
  .caja1{
  
      background: #2C3E50; 
  
  }
  
  .caja2{
      background: #2C3E90; 
      /*Especificamos que sea relative*/
      position: relative;
      /*Entonces agremos un top de 200px*/
      top: 200px; 
  }
  
  .caja3 {
      background: #2C3E40; 
  }
  
  .caja4 {
      background: #2C3E20; 
  }
  ```
  
  Lo que hace es que recorre la caja hacia abajo, puesto que pusimos un top de 20px y top es arriba, lo importante aquí es recalcar que el position relative nos respeta el top que hicimos. 
  
  <img src="file:///home/genaro_javier/Imágenes/Screenshot_20210403_115809.png" title="" alt="Screenshot_20210403_115809.png" data-align="center">
  
  Como se puede ver el espacio del top de la caja 2 es respetado y por lo tanto la caja 3 y 4 no cambian de posición. También podemos usar números negativos. 
  
  Un punto importante a mencionar es que las propiedades top y left son las más importantes por defecto, si nosotros ademas de usar estas dos usamos bottom y right el navegador no los toma en cuenta y se queda con los valores de top y left, en el caso de que no usaramos ni top ni left y usamos bottom y right el navegador SI las toma en consideración. 

- **Absolute**

- **Fixed**

- **Sticky**

### Z-Index

Es como la forma en la que vamos a posicionar un elemento encima de otro, ordena los elementos del eje Z, quien tenga un valor mas alto, estará mas adelante en el eje Z. Es importante recordar que el Z-Index solo funciona cuando las cajas están posicionadas, si no lo están no aplica. 

Por ejemplo, tenemos la caja 2 sobre la caja 3, si nosotros queremos que la caja 3 este sobre la 2. Tan simple como es ponerle su respectivo position: relative;

<img title="" src="file:///home/genaro_javier/Imágenes/Screenshot_20210403_121420.png" alt="Screenshot_20210403_121420.png" data-align="center">

Cuando nosotros usamos el position: relative, las cajas adquieren un nivel de importancia de 0, por lo tanto como caja 1 como la 2 tienen el valor de 0, pero caja 3 sigue estando enfrente debido al flujo de HTML, ya que la caja 3 fue dibujada después. 

<img src="file:///home/genaro_javier/Imágenes/Screenshot_20210403_123002.png" title="" alt="Screenshot_20210403_123002.png" data-align="center">

Lo que necesitamos hacer es poner un valor mayor en Z-Index. 

```css
.caja2{
    background: #2C3E90; 
    position: relative;
    top: 30px;
    left: 20px; 
    z-index: 1; 
}

.caja3 {
    background: #2C3E40; 
    position: relative;
}
```

<img src="file:///home/genaro_javier/Imágenes/Screenshot_20210403_123103.png" title="" alt="Screenshot_20210403_123103.png" data-align="center">

Ahora algo que es muy recomendable al usar Z-Index, es que si queremos ir agregando mas elementos enfrente de otos lo hagamos usando valores lejanos ej. 

```css
.caja1{

    background: #2C3E50; 
    position: relative;
    z-index: 10; 
}

.caja2{
    background: #2C3E90; 
    position: relative;
    top: 30px;
    left: 20px; 
    z-index: 20; 
}

.caja3 {
    background: #2C3E40; 
    position: relative;
    z-index: 30; 
}

.caja4 {
    background: #2C3E20;
    position: relative;
    z-index: 40; 
}
```

```html
<!DOCTYPE html>
<html>
<head>
    <title>Propiedades de Texto</title>
    <link rel="stylesheet" type="text/css" href="css/estilos2.css">
    <link rel="stylesheet" type="text/css" href="css/normalize.css">
</head>
<body>
    <div class="caja1">
        <h1>Caja 1</h1>
    </div>
    <div class="caja2">
        <h1>Caja 2</h1>
    </div>
    <div class="caja3">
        <h1>Caja 3</h1>
    </div>
    <div class="caja4">
        <h1>Caja 4</h1>
    </div>
</body>
```

¿Por qué hacemos esto? Es una buena practica puesto que si queremos agregar otro elemento en medio de por ejemplo caja 3 y 4, tendríamos que modificar todo lo que exista encima de estas cajas. Es recomendable un mínimo de 10 espacios entre cada index, esto a futuro te podría salvar de muchos errores al usar esta propiedad. 

### Padres e Hijos

El padre es el contenedor y el hijo o hijos son los otros elementos que están dentro del padre. 

```html
    <div class="contenedor">
        <div class="hijo">    
        </div>
    </div>
```

El hijo por lo regular siempre estaría dentro del padre pero si nosotros necesitamos que este se posicione detrás de el lo hacemos modificando lo siguiente: 

```css
.contenedor {
    background: orange; 
    height: 300px; 
    width: 300px; 
    margin: 20px;
    /*Dejamos sin position al contenedor*/
}

.hijo {
    background: blue; 
    height: 120px; 
    width: 120px; 
    position: relative;
    bottom: 10px;
    right: 10px; 
    /*Y ponemos -1 en el Z-index*/
    z-index: -1; 
}
```
