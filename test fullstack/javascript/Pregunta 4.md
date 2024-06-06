## Filtrar números pares de  un arreglo

```js
function filtrarPares(numeros) {
  const numerosPares = numeros.filter(numero => numero % 2 === 0);
  console.log(numerosPares);
}

// Ejemplo de uso:
const arregloDeNumeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
filtrarPares(arregloDeNumeros);
```