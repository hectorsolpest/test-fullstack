## Local Storage en JavaScript

```js
function guardarEnLocalStorage(clave, valor) {
  // Guardar el valor en localStorage
  localStorage.setItem(clave, valor);
}

function recuperarDeLocalStorage(clave) {
  // Recuperar el valor de localStorage
  return localStorage.getItem(clave);
}

// Ejemplo de uso:
guardarEnLocalStorage('miClave', 'miValor');
const valorRecuperado = recuperarDeLocalStorage('miClave');

console.log(valorRecuperado); // Muestra 'miValor'

```