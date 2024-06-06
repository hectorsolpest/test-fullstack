## Clave primaria y clave foránea

Clave Primaria (Primary Key): Una clave primaria es un campo o conjunto de campos que identifica de manera única cada fila en una tabla. No puede haber dos filas con la misma clave primaria, y no puede ser null. La clave primaria es esencial para:
- Identificar cada registro de forma única.
- Establecer relaciones con otras tablas.
- Mejorar el rendimiento de las consultas a través de la indexación.

Clave Foránea (Foreign Key): Una clave foránea es un campo o conjunto de campos en una tabla que se refiere a la clave primaria de otra tabla. La relación entre dos tablas se establece mediante la clave foránea. Esto permite:
- Mantener la integridad referencial entre tablas.
- Asegurar que los datos relacionados en diferentes tablas sean consistentes.
- Permitir la navegación entre tablas relacionadas durante las consultas.