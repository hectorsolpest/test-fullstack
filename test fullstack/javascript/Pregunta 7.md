## Promesas en JavaScript

En JavaScript, una Promesa es un objeto que representa la eventual finalización o fracaso de una operación asíncrona. Esencialmente, es un contenedor para un valor que aún no se conoce, pero que se determinará en el futuro1. Las promesas tienen tres estados:

- Pendiente: Estado inicial, ni cumplida ni rechazada.
- Cumplida: Significa que la operación se completó con éxito.
- Rechazada: Significa que la operación falló.

```js
let promesa = new Promise(function(resolve, reject) {
  // Después de 1 segundo, la promesa se cumple con el valor "¡Éxito!"
  setTimeout(function() {
    resolve("¡Éxito!"); // ¡Todo salió bien!
  }, 1000);
});

promesa.then(function(valor) {
  console.log(valor); // Muestra "¡Éxito!" después de 1 segundo.
}, function(razon) {
  console.error(razon); // Muestra un error si algo salió mal.
});

```