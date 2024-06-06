## Crear una base de datos y una tabla

```sql
-- Crear la base de datos company
CREATE DATABASE company;

-- Seleccionar la base de datos para usar
USE company;

-- Crear la tabla employees
CREATE TABLE employees (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100),
  position VARCHAR(50),
  salary DECIMAL(10, 2),
  hire_date DATE
);
```