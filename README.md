# Blog de JavaScript y jQuery

Para añadir una entrada del blog, se debe de crear una carpeta con la fecha y el tiempo en formato ISO: "2022-09-23T22-45", además del título o descripción sencilla de la entrada, de esta manera: "2022-09-23T22-45-js-math". Esta carpeta estará en la sección asignada, ya sea en "javascript"o "jquery".

Dentro de esta carpeta estará solamente el `index.html` y los recursos usados en la entrada a añadir.

De esta manera, si se desea añadir una entrada sobre "Strings" de JavaScript, se creará la carpeta "2022-09-23T22-45-J" en "javascript", y dentro estará el archivo `index.html`: `javascript/2022-09-23T22-45-J/index.html`.


## Template del HTML

Favor copiar siempre el template.html que está en la carpeta root según cada subcarpeta:

- `template-sub0.html` para aquellas entradas que estén en el root: `/` (por lo general no debería de usarse este.)
- `template-sub1.html` para aquellas entradas en una subcarpeta del root: `/javascript/` `/anexos/` `/jquery`, etc.
- `template-sub2.html` para las entradas que ya son contenido en sí, que están dentro de una carpeta del tipo `2022-09-23T22-45-titulo`.

Luego de copiar el template.html según corresponde, renombrarlo a `index.html` y empezar a añadir el contenido al `<article>`.

## Añadir una navegación en el sidebar

Para añadir una navegación en el sidebar de cada entrada, primero es necesario definir el `id` de cada etiqueta de `<h1>`, `<h2>`, `<h3>` y `<h4>` existentes con un nombre que describa la sección.

Luego, en el sidebar se añaden enlaces a cada parte del artículo a través de los IDs antes definidos, de la siguiente manera:

```html
<!-- Sidebar -->
<ul>
  <li>

    <a href="#propiedades-metodos">Propiedades y métodos</a>
    <ul>
      <li><a href="#propiedades">Propiedades</a></li>
      <li><a href="#metodos">Métodos</a></li>
    </ul>

  </li>
</ul>

<!-- Article -->

<h2 id="propiedades-metodos">Propiedades y métodos</h2>
...
<h3 id="propiedades">Propiedades</h3>
...
<h3 id="metodos">Métodos</h3>
...
```

## Código formateado

Se utiliza el programa `pygmentize` (https://pygments.org) para presentar código formateado, el cual se instala con `pip3 install Pygments`.

### Uso con Input-Output

Para usar el programa, en la terminal se escribe:

```
pygmentize -f html -l javascript
```

Entonces, se procederá a escribir el código de JavaScript y se finaliza con la combinación de teclas `CTRL+D`. Posteriormente se imprimirá el código html a incrustar en el artículo.

### Uso con archivo

En caso de querer formatear un archivo de JavaScript ya existente, se utiliza el siguiente comando, el cual obtiene el archivo `entrada.js` y lo formatea hacia el archivo `archivo-final.html`. Se puede omitir la entrada para soicitarlo por medio del teclado y finalizar con `CTRL+D`, o bien se puede omitir el archivo de salida para que el resultado sea impreso en la terminal:

```
pygmentize -f html -l javascript -o archivo-final.html entrada.js
```
