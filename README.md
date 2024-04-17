# Entrega 2. Reactividad programación web II

## Reactividad en Vue

Funciones Ref y Reactive.
La reactividad es uno de los conceptos fundamentales en Vue, permitiendo que los componentes respondan automáticamente a los cambios en los datos. 

### Función ref
La función ref es una de las formas más básicas de crear datos reactivos en Vue. Permite envolver un valor primitivo o un objeto y convertirlo en un objeto reactivable. Cuando el valor envuelto por ref cambia, cualquier componente que esté utilizando ese valor se actualizará automáticamente.

Características principales de ref:
- Envuelve valores primitivos y objetos.
- Devuelve un objeto envuelto que contiene la propiedad .value para acceder y modificar el valor.
- Se utiliza comúnmente para valores individuales.
Función reactive

### Función reactive
Es otra forma de crear datos reactivos, pero a diferencia de ref, se utiliza principalmente para objetos complejos. Al envolver un objeto con reactive, todos sus miembros se vuelven reactivos, lo que significa que cualquier cambio en cualquiera de sus propiedades se reflejará automáticamente en los componentes que lo utilizan.

Características principales de reactive:
- Envuelve objetos complejos.
- Todos los miembros del objeto se vuelven reactivos.
- Devuelve un proxy del objeto original.


### Diferencias entre ref y reactive

- Uso: ref se utiliza principalmente para valores individuales, mientras que reactive se utiliza para objetos complejos.

- Sintaxis: ref devuelve un objeto envuelto con una propiedad .value, mientras que reactive devuelve un proxy del objeto original.

- Gestión de la reactividad: ref es más adecuado para datos primitivos o valores individuales, mientras que reactive es más adecuado para objetos complejos con múltiples propiedades.

Ejemplos funcionando de cada una de ellas.
[Ejemplo con ref](Vue/src/components/UsernameInputRef.vue)
[Ejemplo con reactive](Vue/src/components/UsernameInputReactive.vue)


Computed y Watch. Ejemplos de uso funcionando de cada una.


Reactividad en Svelte (4 puntos)

Dos ejemplos funcionando con declaraciones reactivas en Svelte.