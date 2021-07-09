# Especificidad

Se refiere a la importancia con la que se aplican los estilos a los elementos. CSS se hace llamar estilos en cascada, esto nos da a entender que los cambios se aplican de arriba hacia abajo es decir si tengo el siguiente código: 

```css
h1 {
    color: red; 
}

h1 {
    color: blue; 
}
```

Se aplicara primero el color rojo, seguido el color azul, este cambio pasa tan rápido que no es posible verlo a simple vista, incluso el navegador no permite visualizar el cambio, lo que nos hace pensar que el color azul fue el que se aplico debido a la cascada, de alguna manera esta forma de verlo es correcta, pero es importante saber que existe esto. Entonces siguiendo con el tema de especificidad la jerarquía queda de la siguiente manera. 

| !Important                       |
| -------------------------------- |
| Estilos en linea                 |
| Identificadores                  |
| Clases, Pseudo-Clases, Atributos |
| Elementos                        |
| Pseudo-Elementos                 |

Por ende si tenemos el siguiente código: 

```css
h1 {
    color: blue; 
}
.clase-ejemplo {
    color: red; 
}
```

Aquí no existe cascada, pero si especificidad puesto que la clase tiene mayor jerarquía que un elemento, se aplica el código para la clase y no el elemento. 

# # Metodología de BEM

La metodología de bem, nos ayuda a que nuestro código sea mas facil de leer y tenga una mejor estructura, consiste en poner un nombre en general adjunto de un elemento en especifico ej. 

```html
<!-- Tenemos un divisor con la clase "contact-form" 
esta metodología nos dice que debemos llamar a las demas clases
iniciando con el nombre de la que las contiene-->
<div class="contact-form">
<!-- Entonces si tenemos un formulario y a sus elementos
queremos darle otros estilos, debemos de llamarlos por la misma
clase seguido de dos __ y despues el elemento, es importante 
recordad que los dos guienes se ponen por bloques-->
        <input type="text" class="contact-form__input"><br>
<!--Si tuviesemos algo como lo siguiente, podemos observar que
seguido del primer elemento, se le asigna un solo guión, 
con el nombre del elemento que esta dentro-->
<p><h2 class="contact-form__p-h2">Ingresar nombre</h2></p>
<!--Si despues queremos aplicar diferentes estilos ya sea por x 
razón podemos poner dos guiónes medio y una palabra que de 
preferencia lo describa-->
        <input type="text" class="contact-form__input--active"><br>
        <input type="password" class="contact-form__input">
        <input type="text" class="contact-form__input"><br>
    </div>
```

```css
.contact-form__input--active{
    color: red; 
}
.contact-form__input{
    color: blue; 
}
```
