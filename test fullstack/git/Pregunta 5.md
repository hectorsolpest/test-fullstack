## Merge conflict

Un “merge conflict” o conflicto de fusión en Git ocurre cuando dos ramas tienen cambios que no pueden ser combinados automáticamente. Esto suele suceder cuando dos desarrolladores han editado las mismas líneas en un archivo o cuando uno ha modificado un archivo y el otro lo ha eliminado. Git no puede decidir qué cambios conservar, por lo que requiere intervención manual para resolver el conflicto2.

Para resolver un conflicto de fusión, se pueden seguir estos pasos:

- Identificar los archivos en conflicto: Git marcará los archivos que tienen conflictos. Se puede usar el comando git status para ver cuáles son.

- Editar los archivos para resolver los conflictos: Abrir los archivos en conflicto en el editor de texto y buscar las marcas de conflicto que Git ha añadido. Ver secciones marcadas con <<<<<<<, =======, y >>>>>>>. Estas marcas dividen los cambios del archivo que están en conflicto.

- Decidir qué cambios conservar: Se deben revisar los cambios y decidir mantener los cambios de una rama, de la otra, o combinarlos de alguna manera. Luego, eliminar las marcas de conflicto.

- Añadir los archivos resueltos: Una vez que resueltos los conflictos, usar git add para marcar los archivos como resueltos.

- Hacer un commit: Finalmente, realizar un commit con los cambios resueltos. Git permitirá fusionar las ramas una vez que todos los conflictos hayan sido resueltos y añadidos al índice.
