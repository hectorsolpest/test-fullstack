## DOM en JavaScript

El DOM (Document Object Model o Modelo de Objetos del Documento) es una representación estructurada de los documentos HTML, XML o SVG como un árbol de nodos en la memoria. En el contexto de las páginas web, el DOM permite que JavaScript interactúe con el contenido, la estructura y el estilo de la página.

- Seleccionar elementos: Para manipular un elemento, primero se debe seleccionar. Se puede hacer utilizando métodos como document.getElementById(), document.querySelector(), o document.getElementsByClassName().

- Modificar contenido: Una vez que se tiene una referencia a un elemento, se puede cambiar su contenido interno con la propiedad textContent o innerHTML.

- Cambiar estilos: También se pueden cambiar los estilos CSS de un elemento directamente a través de la propiedad style.

- Añadir o eliminar elementos: Se pueden crear nuevos nodos con document.createElement() y añadirlos al DOM con appendChild() o insertBefore(). Para eliminar, se puede usar removeChild().

- Eventos: Los eventos permiten ejecutar código en respuesta a ciertas acciones del usuario, como clics o pulsaciones de teclas. Se pueden añadir manejadores de eventos usando addEventListener().
