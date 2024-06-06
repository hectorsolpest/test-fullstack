## Diferencia entre var, let y const

- var: Es la forma más antigua de declarar variables. Tiene alcance de función , lo que significa que si se declara una variable con var dentro de una función, solo es accesible dentro de esa función. Fuera de funciones, var tiene alcance global. Además, var se eleva, lo que significa que se puede usar la variable antes de declararla; sin embargo, su valor será undefined hasta que se ejecute la declaración.

- let: Permite declarar variables con alcance de bloque, es decir, solo son accesibles dentro del bloque donde se declaran. A diferencia de var, let no se eleva, por lo que si se intenta usar una variable let antes de declararla, se obtendrá un error de referencia.

- const: Se utiliza para declarar constantes con alcance de bloque. Una vez que se asigna un valor a una variable const, no se le puede reasignar otro valor. Al igual que let, const no se eleva y debe ser inicializado en el momento de la declaración.