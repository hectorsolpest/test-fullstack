## Ejemplo de transacción en MySQL

Una transacción en MySQL es un conjunto de operaciones que se ejecutan como una sola unidad lógica de trabajo. Este proceso garantiza que todas las operaciones dentro de la transacción se completen con éxito o ninguna se complete, lo que ayuda a mantener la integridad de los datos en una base de datos.

```sql 
START TRANSACTION;

-- Supongamos que queremos actualizar el salario de un empleado y registrar este cambio
UPDATE employees SET salary = 75000 WHERE id = 1;
INSERT INTO salary_changes(employee_id, old_salary, new_salary, change_date)
VALUES (1, 70000, 75000, NOW());

-- Si ambas operaciones son correctas, confirmamos la transacción
COMMIT;

-- Si hay un error y no queremos aplicar los cambios, revertimos la transacción
ROLLBACK;
```