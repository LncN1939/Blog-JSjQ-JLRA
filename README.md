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
