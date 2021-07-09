# Unidades de Medidas

En CSS tenemos dos unidades de medida,  las que son: 

- **Fijas** Son los px, los mm, los puntos, los cm, etc. 

- **Relativas** Estas dependen de algo "Variables", este tipo de variables nos sirven para poder hacer responsive las paginas. 
  
  **em** Es una unidad de medida de tipo relativa, que por defecto son 16px, esta medida es dada por el navegador, hay algunos que varían el valor de un em, pero uno que otro navegador podria variar este valor. 
  
  **¿Pero como hacemos para que esa medida la definamos nosotros?** 
  
  Muy bien pues este tipo de medida se **Hereda** el contenedor es el que define el valor del em. 
  
  $$
  5em = 16 * 5 = 80px
  $$
  
  Ahora bien, por ejemplo nosotros tenemos el siguiente código: 
  
  ```html
  <!-- Tenemos nuestro contenedor -->
  <div class="contact-form--2">
  <!-- Y dos elementos dentro del contenedor-->
          <h2 class="contact-form-2__h2">Titulo</h2>
          <h2 class="contact-form-2__h2-2">Titulo</h2>
      </div>
  ```
  
  ```css
  /*Estilos para el contenedor*/
  .contact-form--2{
  /*Notese que le estamos agregando una medida de 10px al
  contenedor*/
      font-size: 10px; 
      background:green;
  }
  
  /*Los siguientes son estilos para los h2, pero en lugar de
  usar px usamos em*/
  .contact-form-2__h2{
  /*Es muy importante recalcar que como es una medida heredada
  la unidad em sera igual a la especificada en el contenedor
  en este caso 1em sera igual a 10px*/
      font-size: 2em; /*2em = 20px*/
      color: red; 
  }
  
  .contact-form-2__h2-2{
      font-size: 2em; /*2em = 20px*/
      color: blue; 
  }
  ```

### VW y VH

Estas también son medidas relativas y funcionan como los porcentajes

- **VW** modifica el largo de la caja. 
  
  ![Screenshot_20210331_230052.png](/home/genaro_javier/Imágenes/Screenshot_20210331_230052.png)

- **VH** modifica el ancho de la caja
  
  ![Screenshot_20210331_232011.png](/home/genaro_javier/Imágenes/Screenshot_20210331_232011.png)

# Propiedades

- **font-size** Cambia el tamaño de la letra 
