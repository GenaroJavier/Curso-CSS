# Propiedades de texto

- **font-size** Tamaño de letra

- **font-family** Tipografía 

- **line-height** Esta propiedad no especifica el espacio que hay entre el texto y la caja que rodea al texto ej. 
  
  **Con line-height = 1**
  
  ![](/home/genaro_javier/.config/marktext/images/2021-04-01-00-01-13-image.png)
  
  **Con line-height = 2**
  
  ![](/home/genaro_javier/.config/marktext/images/2021-03-31-23-59-52-image.png)

- **font-weight** Es el grosor de la letra. 

- Si queremos agregar un tipografía de Internet podemos acceder a [Google Fonts](https://fonts.google.com/?preview.text_type=custom), escoger una fuente, ir al apartado de **selected families** y copiar el link de HTML y CSS y pegarlos donde corresponde. 
  
  ![](/home/genaro_javier/.config/marktext/images/2021-04-01-00-19-35-image.png)

```html
<head>
    <title>Propiedades de Texto</title>
    <link rel="stylesheet" type="text/css" href="css/estilos2.css">
    <!--Fuentes-->
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Yatra+One&display=swap"  rel="stylesheet">
</head>
```

```css
.contact-form--2__h1 {
    font-size: 2em; /*Tamaño del texto*/
    line-height: 1; /*Espacio hacia arriba y abajo*/
    font-weight: 700; /*Grosor de letra*/
    font-family: 'Yatra One', cursive; /*Fuente, cabe mencionar
que se encuentran dos tipos de fuentes separadas por una coma, puesto
que en el caso de no contar con conexión se utiliza la 2da fuente*/
    color: #39C700; /*Color*/
}
```
