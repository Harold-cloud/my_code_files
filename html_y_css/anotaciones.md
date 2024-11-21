## Padding
El padding es una propiedad de estilo de css para modificar el tamaño de las etiquetas HTML que tengan el modelo de caja como el `<div>`. El padding se aplica de la siguiente forma `padding: 16px 8px 4px 8px;` haciendo referencia a las posiciones arriba, derecha, abajo, izquierda en ese orden, si se aplica un solo valor indica que todas las posiciones valen ese valor, si se aplican dos valores el primer valor es arriba, abajo y el segundo valor es izquierda, derecha. El tamaño de las cajas las determina el padding, la altura y el ancho del contenido y el border.

## Position
static --> default, relative--> father, absolute--> child, fixed--> vh(viewport=pantalla), sticky-->father

z-index y contexto de apilamiento

## Flexbox
Flexbox es un modelo de diseño unidimensional para distribuir los espacios entre los elementos.
flexbox tiene distintas propiedades para uso empezando por:

`display: block;` Hace que los elementos html se comporten como cajas o bloques, y viene por 
default.

`display: inline;` Hace que los elementos HTML se comporten como texto, permitiendo que otros elementos estén a su lado. La altura y el ancho no se aplican a los elementos inline.

`display: flex;` Se usa en el contenedor (padre) para activar Flexbox y permitir la distribución eficiente de los elementos hijos en una dirección específica (por defecto, en filas).

`flex-direction: row;` Coloca los elementos hijos en una dirección de fila (horizontal). Este es el valor por defecto.

`flex-direction: column` Coloca los elementos hijos en una dirección de columna (vertical).

`flex-direction: row-reverse` Coloca los elementos hijos en una dirección de fila pero invierte el orden.

`flex-direction: column-reverse` Coloca los elementos hijos en una dirección de columna pero invierte el orden.

`flex-direction: flex;` funciona igual que `display: flex;`.

`direction: rtl;`  Indica la dirección de escritura del texto, en este caso, de derecha a izquierda (right to left).

`writing-mode: vertical-lr` Coloca los elementos en una dirección vertical de columna, pero con el contenido alineado de izquierda a derecha.

`flex-wrap: nowrap;` Ajusta el contenido del contenedor manteniendo a los elementos hijos se mantendrán en una sola línea sin importar si hay suficiente espacio o no. Este es el valor por defecto.

`flex-wrap: wrap;` Cuando no hay suficiente espacio en una línea, los elementos se moverán a la siguiente línea, haciendo que el contenedor sea más alto. 

`flex-wrap: row nowrap;` Combina las propiedades flex-direction y flex-wrap en una sola declaración. Esto facilita la especificación de ambas propiedades de forma más concisa y clara.

`flex-grow: 1;` Se utiliza dentro de un contenedor flex para definir cómo deben crecer los elementos hijos cuando hay espacio adicional disponible. Cuando tiene el valor en 0 significa que los elementos no creceran.

`flex-shrink: 1;` Se usa para definir cómo deben reducirse los elementos hijos dentro de un contenedor Flexbox cuando hay menos espacio disponible que el necesario para acomodarlos.

`flex-basis: auto;`  controla cuánto se reducirá un elemento cuando el espacio es limitado en el contenedor Flexbox.

 `flex: auto;`  Es una forma abreviada de establecer los valores de flex-grow, flex-shrink, y flex-basis en una sola declaración. `flex: 1 1 100px; --> flex-grow: 1; --> flex-shrink: 1; --> flex-basis: 100px;`

 `order:` Especifica el orden en el que se muestran los elementos en un contenedor flex. Los elementos con un valor menor de order aparecerán antes que los elementos con un valor mayor.

### justify-content

 `justify-content:` Funciona a nivel de filas.

 | **Valor**            | **Descripción**                                                                                       | **Ejemplo de CSS**                     |
|----------------------|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| `flex-start`         | Alinea los elementos al inicio del eje principal.                                                    | `justify-content: flex-start;`       |
| `flex-end`           | Alinea los elementos al final del eje principal.                                                     | `justify-content: flex-end;`         |
| `center`             | Alinea los elementos en el centro del eje principal.                                                 | `justify-content: center;`           |
| `space-between`     | Distribuye el espacio entre los elementos, dejando el primer elemento al inicio y el último al final. | `justify-content: space-between;`    |
| `space-around`      | Distribuye el espacio alrededor de los elementos, con espacio igual a ambos lados de cada elemento. | `justify-content: space-around;`     |
| `space-evenly`      | Distribuye el espacio de manera equitativa entre todos los elementos, incluyendo el espacio al inicio y al final. | `justify-content: space-evenly;`     |
| `start`              | Alinea los elementos al inicio del contenedor, basado en la dirección de escritura del contenedor.   | `justify-content: start;`            |
| `end`                | Alinea los elementos al final del contenedor, basado en la dirección de escritura del contenedor.     | `justify-content: end;`              |
| `left`               | Alinea los elementos al inicio del contenedor (equivalente a `flex-start` en `row` o `start` en `ltr`). | `justify-content: left;`             |
| `right`              | Alinea los elementos al final del contenedor (equivalente a `flex-end` en `row` o `end` en `ltr`).    | `justify-content: right;`            |


`gap:<size>px` En CSS se usa para definir el espacio entre elementos en contenedores flexibles y en cuadrículas. La propiedad gap permite especificar ambos espacios (columnas y filas) en una sola línea. El primer valor es para grid-column-gap y el segundo para grid-row-gap. Si solo se proporciona un valor, se aplica a ambos.

### align-content

`align-content:` Funciona a nivel de columnas. (no es tan usado).

| **Valor**            | **Descripción**                                                                                         | **Ejemplo de CSS**                |
|---------------------|---------------------------------------------------------------------------------------------------------|----------------------------------|
| `flex-start`        | Alinea el contenido al inicio del contenedor.                                                           | `align-content: flex-start;`     |
| `flex-end`          | Alinea el contenido al final del contenedor.                                                             | `align-content: flex-end;`       |
| `center`            | Alinea el contenido en el centro del contenedor.                                                         | `align-content: center;`         |
| `space-between`    | Distribuye el espacio entre las líneas de contenido, dejando el primer contenido al inicio y el último al final. | `align-content: space-between;`  |
| `space-around`     | Distribuye el espacio alrededor de las líneas de contenido, con espacio igual alrededor de cada línea. | `align-content: space-around;`   |
| `space-evenly`     | Distribuye el espacio de manera equitativa entre todas las líneas de contenido, incluyendo el espacio al inicio y al final. | `align-content: space-evenly;`   |
| `stretch`           | Estira las líneas de contenido para llenar el contenedor, ajustando la altura de las líneas.                | `align-content: stretch;`        |
| `start`             | Alinea el contenido al inicio del contenedor, basado en la dirección de escritura del contenedor.             | `align-content: start;`          |
| `end`               | Alinea el contenido al final del contenedor, basado en la dirección de escritura del contenedor.               | `align-content: end;`            |
| `baseline`          | Alinea las líneas de contenido según sus líneas base de texto.                                                | `align-content: baseline;`       |
| `last baseline`     | Alinea la línea de contenido en la última línea base.                                                       | `align-content: last baseline;`  |

### align-items

`align-items:` Se utiliza para alinear los elementos dentro de un contenedor flexbox o grid a lo largo del eje transversal, es decir, el eje perpendicular al eje principal. Esta propiedad afecta a los elementos dentro de una sola línea en un contenedor flex o a las filas/columnas en un contenedor grid.

| **Valor**         | **Descripción**                                                                                         | **Ejemplo de CSS**                |
|------------------|---------------------------------------------------------------------------------------------------------|----------------------------------|
| `flex-start`     | Alinea los elementos al inicio del contenedor en el eje transversal.                                    | `align-items: flex-start;`       |
| `flex-end`       | Alinea los elementos al final del contenedor en el eje transversal.                                      | `align-items: flex-end;`         |
| `center`         | Alinea los elementos en el centro del contenedor en el eje transversal.                                  | `align-items: center;`           |
| `baseline`       | Alinea los elementos a lo largo de la línea base de texto de los elementos.                              | `align-items: baseline;`         |
| `stretch`        | Estira los elementos para que ocupen todo el espacio disponible en el eje transversal.                   | `align-items: stretch;`          |
| `start`          | Alinea los elementos al inicio del contenedor, basado en la dirección de escritura del contenedor.        | 
 `align-items: start;` |

### align-self

`align-self:` Permite a un elemento específico en un contenedor flexbox o grid anular el comportamiento de alineación establecido por la propiedad align-items del contenedor. Esta propiedad controla cómo se alinea un elemento individual a lo largo del eje transversal del contenedor.


| **Valor**        | **Descripción**                                                                                         | **Ejemplo de CSS**               |
|-----------------|---------------------------------------------------------------------------------------------------------|---------------------------------|
| `auto`           | Usa el valor de `align-items` del contenedor padre (valor predeterminado).                             | `align-self: auto;`             |
| `flex-start`     | Alinea el elemento al inicio del contenedor en el eje transversal.                                     | `align-self: flex-start;`      |
| `flex-end`       | Alinea el elemento al final del contenedor en el eje transversal.                                       | `align-self: flex-end;`        |
| `center`         | Alinea el elemento en el centro del contenedor en el eje transversal.                                   | `align-self: center;`          |
| `baseline`       | Alinea el elemento a lo largo de la línea base de texto de los elementos.                               | `align-self: baseline;`        |
| `stretch`        | Estira el elemento para que ocupe todo el espacio disponible en el eje transversal.                      | `align-self: stretch;`         |
| `start`          | Alinea el elemento al inicio del contenedor, basado en la dirección de escritura del contenedor.         | `align-self: start;`           |
| `end`            | Alinea el elemento al final del contenedor, basado en la dirección de escritura del contenedor.           | `align-self: end;`             |
| `self-start`     | Alinea el elemento al inicio del contenedor, en función de la dirección del contenido.                    | `align-self: self-start;`      |
| `self-end`       | Alinea el elemento al final del contenedor, en función de la dirección del contenido.                      | `align-self: self-end;`        |


## Grid

`display: grid` 

`grid-template-columns:`  Es una propiedad de CSS que se utiliza para definir las columnas de un grid en un diseño CSS Grid Layout. Esta propiedad especifica el número de columnas, así como su tamaño y comportamiento. Cada valor representa una columna en el grid. Puedes usar varias unidades de medida para definir el tamaño de las columnas.

| Argumento       | Descripción                                                                                   | Ejemplo                                      |
|-----------------|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| Longitudes fijas | Especifica el tamaño fijo de las columnas usando unidades como `px`, `em`, `rem`, etc.        | `grid-template-columns: 100px 200px 300px;`  |
| Porcentajes     | Especifica el tamaño relativo al contenedor del grid usando porcentajes.                      | `grid-template-columns: 50% 50%;`            |
| Fracciones (`fr`)| Usa fracciones del espacio disponible en el contenedor del grid.                             | `grid-template-columns: 1fr 2fr;`            |
| Auto            | Ajusta automáticamente el tamaño de la columna según su contenido y espacio.                            | `grid-template-columns: auto auto;`          |
| `minmax(min, max)`| Define un tamaño mínimo y máximo para una columna.                                          | `grid-template-columns: minmax(100px, 1fr);` |
| `repeat(count, value)`| Crea múltiples columnas con el mismo tamaño.                                            | `grid-template-columns: repeat(3, 1fr);`     |


`grid-template-rows:` En CSS se utiliza para definir las filas de un grid en un diseño CSS Grid Layout. Esta propiedad especifica el número de filas, así como su tamaño y comportamiento. Cada valor representa una fila en el grid. Puedes usar varias unidades de medida para definir el tamaño de las filas. Usa los mismos argumentos que `grid-template-columns` solo que en este caso va para las filas.

>Nota:
> **En grid se pueden crear cuadriculas sin la necesidad de tener elementos.**

`grid-auto-rows:` Se utiliza para especificar el tamaño de las filas implícitas creadas por el grid container cuando no se definen todas las filas explícitamente en la propiedad grid-template-rows. Esto es útil cuando tienes más elementos en tu grid de los que has definido explícitamente en grid-template-rows.

`minmax(min, max)` En CSS Grid Layout es una herramienta poderosa que permite definir un tamaño mínimo y máximo para las columnas o filas en un contenedor de grid. 

`auto-fill;` Permite que las columnas o filas se rellenen automáticamente con tantos elementos como sea posible, ajustándose al contenedor. 

`auto-fit;` Permite que las columnas o filas ocupen el espacio ajustandolo hasta los limites con la cantidad de elementos, llenando al contenedor. 

`grid-column-start` y `grid-column-end` Te permiten especificar en qué líneas de la cuadrícula comienzan y terminan los elementos de la cuadrícula. Estas propiedades te permiten definir el tamaño y la posición de los elementos de manera precisa. Tienes varias maneras de representarse en la sintaxis de css.

```
grid-column-start: 2;  /* Comienza en la línea 2 */
grid-column-end: span 3; /* Termina después de 3 líneas */
grid-column: 2 / 4; /* Equivalente a grid-column-start: 2; grid-column-end: 4; */
```

### grid-area

```
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 100px);
    gap: 10px;
    grid-template-areas:
        "header header header"
        "sidebar main main";
}

.header {
    grid-area: header;
}

.sidebar {
    grid-area: sidebar;
}

.main {
    grid-area: main;
}
```

### justify-items

`justify-items` se utiliza para alinear los elementos de la cuadrícula a lo largo del eje horizontal (es decir, a lo largo de las filas). Esta propiedad afecta a todos los elementos dentro de un contenedor de cuadrícula. 

`start`: Alinea los elementos al inicio del contenedor de la cuadrícula.
`end:`Alinea los elementos al final del contenedor de la cuadrícula.
`center`: Alinea los elementos en el centro del contenedor de la cuadrícula.
`stretch`: Estira los elementos para que ocupen todo el espacio disponible (este es el valor por defecto).

| Valor     | Descripción                                        | Ejemplo CSS              |
|-----------|----------------------------------------------------|--------------------------|
| `start`   | Alinea los elementos al inicio del contenedor      | `justify-items: start;`  |
| `end`     | Alinea los elementos al final del contenedor       | `justify-items: end;`    |
| `center`  | Alinea los elementos en el centro del contenedor   | `justify-items: center;` |
| `stretch` | Estira los elementos para ocupar todo el espacio   | `justify-items: stretch;` (valor por defecto) |


### justify-self 

`justify-self` en CSS Grid se utiliza para alinear individualmente los elementos de la cuadrícula a lo largo del eje horizontal (es decir, a lo largo de las filas) dentro de sus respectivas celdas. Esto proporciona un control más granular sobre la alineación de cada elemento en comparación con justify-items, que afecta a todos los elementos de la cuadrícula.

start: Alinea el elemento al inicio de la celda.
end: Alinea el elemento al final de la celda.
center: Alinea el elemento en el centro de la celda.
stretch: Estira el elemento para que ocupe todo el espacio disponible en la celda (este es el valor por defecto).

| Valor     | Descripción                                        | Ejemplo CSS              |
|-----------|----------------------------------------------------|--------------------------|
| `start`   | Alinea el elemento al inicio de la celda           | `justify-self: start;`   |
| `end`     | Alinea el elemento al final de la celda            | `justify-self: end;`     |
| `center`  | Alinea el elemento en el centro de la celda        | `justify-self: center;`  |
| `stretch` | Estira el elemento para ocupar todo el espacio     | `justify-self: stretch;` (valor por defecto) |


### place-content

`place-content` en CSS Grid es una forma abreviada de establecer tanto align-content como justify-content simultáneamente. Estas propiedades controlan la distribución del espacio entre y alrededor de los elementos de la cuadrícula a lo largo de los ejes vertical (columna) y horizontal (fila), respectivamente.

center: Centra el contenido de la cuadrícula en ambos ejes.
start: Alinea el contenido de la cuadrícula al inicio en ambos ejes.
end: Alinea el contenido de la cuadrícula al final en ambos ejes.
stretch: Estira el contenido de la cuadrícula para ocupar todo el espacio disponible en ambos ejes (este es el valor por defecto).
space-between: Distribuye el contenido de la cuadrícula con espacio igual entre los elementos en ambos ejes.
space-around: Distribuye el contenido de la cuadrícula con espacio igual alrededor de los elementos en ambos ejes.
space-evenly: Distribuye el contenido de la cuadrícula con espacio igual entre y alrededor de los elementos en ambos ejes.

| Valor            | Descripción                                                | Ejemplo CSS                                 |
|------------------|------------------------------------------------------------|---------------------------------------------|
| `center`         | Centra el contenido de la cuadrícula en ambos ejes         | `place-content: center center;`             |
| `start`          | Alinea el contenido al inicio en ambos ejes                | `place-content: start start;`               |
| `end`            | Alinea el contenido al final en ambos ejes                 | `place-content: end end;`                   |
| `stretch`        | Estira el contenido para ocupar todo el espacio            | `place-content: stretch stretch;` (por defecto) |
| `space-between`  | Distribuye el contenido con espacio igual entre elementos  | `place-content: space-between space-between;` |
| `space-around`   | Distribuye el contenido con espacio igual alrededor de elementos | `place-content: space-around space-around;` |
| `space-evenly`   | Distribuye el contenido con espacio igual entre y alrededor de elementos | `place-content: space-evenly space-evenly;` |


>Nota
>Content es el contenido de los elementos y el items es cada elemento individual.








