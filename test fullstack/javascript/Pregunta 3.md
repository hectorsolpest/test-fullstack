## Event Loop

El Event Loop es un concepto fundamental en JavaScript que permite la ejecución de código, la recopilación y procesamiento de eventos, y la ejecución de subtareas en cola de manera eficiente y sin bloquear el hilo principal de ejecución.

Esto significa que una función se ejecutará de principio a fin sin interrupciones. Una desventaja de este modelo es que si un mensaje toma demasiado tiempo para procesarse, puede bloquear la interfaz de usuario, impidiendo que se procesen interacciones como clics o desplazamientos. Para evitar esto, es importante usar operaciones asíncronas y promesas para tareas largas.

En resumen, el Event Loop permite que JavaScript, que es un lenguaje de programación de un solo hilo, maneje operaciones asíncronas y no bloqueantes, dando la ilusión de multithreading a través de la gestión eficiente de tareas y eventos