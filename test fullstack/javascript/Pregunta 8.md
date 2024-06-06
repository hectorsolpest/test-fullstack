## Obtención de datos de una api

```js
function obtenerDatos() {
  fetch('https://api.ejemplo.com/datos')
    .then(function(respuesta) {
      // Convertir la respuesta a JSON
      return respuesta.json();
    })
    .then(function(datos) {
      // Mostrar los datos en el elemento con el id #result
      document.getElementById('result').textContent = JSON.stringify(datos);
    })
    .catch(function(error) {
      // Manejar cualquier error que ocurra durante la petición
      console.error('Error al obtener los datos:', error);
    });
}
```