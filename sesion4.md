<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4

# Actividad: Creación componente de lista de elementos.
Crear un componente de React llamado List que renderice una lista de elementos. El componente debe aceptar una prop llamada items que debe ser un array de objetos. Cada objeto del array debe tener los siguientes campos:

* name: El nombre del elemento.
* color: El color del elemento.

El componente debe renderizar una lista de elementos con el siguiente formato:

```html
<li style={{ color: item.color }}>
<h3>{item.name}</h3>
</li>
``` 

## Requisitos de la actividad:
 * El componente debe ser un componente funcional.
 * El componente debe utilizar props para recibir la lista de elementos.
 * El componente debe renderizar correctamente la lista de elementos.


# Solución