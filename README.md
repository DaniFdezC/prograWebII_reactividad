# Entrega 2. Reactividad programación web II

## Reactividad en Vue

### Funciones Ref y Reactive.
La reactividad es uno de los conceptos fundamentales en Vue, permitiendo que los componentes respondan automáticamente a los cambios en los datos. 

#### Función ref
La función ref es una de las formas más básicas de crear datos reactivos en Vue. Permite envolver un valor primitivo o un objeto y convertirlo en un objeto reactivable. Cuando el valor envuelto por ref cambia, cualquier componente que esté utilizando ese valor se actualizará automáticamente.

Características principales de ref:
- Envuelve valores primitivos y objetos.
- Devuelve un objeto envuelto que contiene la propiedad .value para acceder y modificar el valor.
- Se utiliza comúnmente para valores individuales.
Función reactive

#### Función reactive
Es otra forma de crear datos reactivos, pero a diferencia de ref, se utiliza principalmente para objetos complejos. Al envolver un objeto con reactive, todos sus miembros se vuelven reactivos, lo que significa que cualquier cambio en cualquiera de sus propiedades se reflejará automáticamente en los componentes que lo utilizan.

Características principales de reactive:
- Envuelve objetos complejos.
- Todos los miembros del objeto se vuelven reactivos.
- Devuelve un proxy del objeto original.


#### Diferencias entre ref y reactive

- Uso: ref se utiliza principalmente para valores individuales, mientras que reactive se utiliza para objetos complejos.

- Sintaxis: ref devuelve un objeto envuelto con una propiedad .value, mientras que reactive devuelve un proxy del objeto original.

- Gestión de la reactividad: ref es más adecuado para datos primitivos o valores individuales, mientras que reactive es más adecuado para objetos complejos con múltiples propiedades.

#### Ejemplos funcionando de cada una de ellas. <br>
[Ejemplo con ref](Vue/src/components/UsernameInputRef.vue) <br>
[Ejemplo con reactive](Vue/src/components/UsernameInputReactive.vue) <br>


### Computed y Watch. Ejemplos de uso funcionando de cada una.

#### Computed
Son propiedades que se derivan de otras propiedades reactivas. Se actualizan automáticamente cuando cambian las propiedades en las que dependen. Son útiles para realizar operaciones de cálculo o transformación en los datos del componente de forma reactiva y eficiente.
[Ejemplo con computed](Vue/src/components/UsernameInputComputed.vue) <br>

#### Watch
Permiten observar cambios en una propiedad y reaccionar a ellos ejecutando una función definida por el usuario. Esto es útil cuando necesitas realizar operaciones más complejas o asincrónicas en respuesta a cambios en los datos.
[Ejemplo con watch](Vue/src/components/UsernameInputWatch.vue) <br>

## Reactividad en Svelte

Dos ejemplos funcionando con declaraciones reactivas en Svelte.

[Ejemplo 1 - Comprobador de usuarios](Svelte/src/components/UsernameInputReactive.svelte) <br>
[Ejemplo 2 - Lista de tareas](Svelte/src/components/TaskList.svelte) <br>