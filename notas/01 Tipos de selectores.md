# Tipos de Selectores

- **Universal** Afecta a todos los elementos del HTML. 
  
  ```css
  * {
  
  }
  ```

- **De Tipo** Afecta a todos los elementos del HTML de tipo especificado, que no cuenten con clases, id, etc. 
  
  ```css
  h1 {
  
  }
  ```

- **Clases** 
  
  Lo declaras de esta forma en HTML, nota que pones como atributo la palabra class seguida de un valor el cual es el nombre de clase. 
  
  ```html
  <h1 class="clase-1" >Titulo</h1>
  ```
  
  Lo declaras de esta forma en HTML, nota que pones como atributo la palabra class seguida de un valor el cual es el nombre de clase.
  
  ```css
  .clase-1 {
      color: red; 
  }
  ```

- **ID** El uso de identificadores (IDs) es parecido al de clases, la diferencia radica en el uso que les demos, puesto que el objetivo principal del por que usar un Id, es para referenciar un elemento único. 
  
  ```html
  <h1 id="titulo-principal" >Titulo</h1>`
  ```
  
  ```css
  .titulo-principal {
      color: blue; 
  }
  ```

- **Por atributo** Este tipo de selector de igual forma es parecido a las clases y los IDs, no precisamente es para usar en un único elemento, si no que se caracteriza por ser cualquier palabra como atributo en un elemento de HTML ej. 
  
  ```html
  <h1 tit-gen="titulo-genaro" >Titulo</h1>
  ```
  
  ```css
  [tit-gen="titulo-genaro"] {
      color: green; 
  }
  ```

- **Descendiente** Si tenemos una etiqueta dentro de otra podemos utilizarlas de en CSS de forma descendiente, esto quiere decir que la etiqueta contenedora de otra, se coloca primero ej. 
  
  ```html
  <h1><b>Titulo en negritas</b></h1>
  ```
  
  ```css
  h1 b {
      color: orange; 
  }
  ```

- **Pseudo-Clases** Estas son como disparar un evento cuando realizamos algo, por ejemplo si pasamos el puntero sobre no se, quizás el titulo, este automáticamente se cambie de color.
  
  ```css
  h1 b:hover {
      color: blue; 
  }
  ```

- **Important** En la especificidad es el rango mas alto, el código CSS adjunto con la etiqueta !important si o si se va a aplicar. 
  
  ```css
  h1 {
      color: blue !important; 
  }
  ```

### Notas

CSS significa Cascading Stylesheets o en español por si no manejas el ingles, se traduce como Hojas de estilo en cascada.  
