## Revertir cambios en git

Para revertir el último commit en Git y mantener los cambios en tu área de trabajo, se puede utilizar el comando git reset con la opción --soft seguido de HEAD~1

```console
git reset --soft HEAD~1
```

Este comando moverá el puntero HEAD al commit anterior, pero dejará los cambios actuales en el área de trabajo, permitiendo modificarlos y volver a hacer commit si es necesario.
Si se desea deshacer el último commit y eliminar todos los cambios, se puede usar la opción --hard

```console
git reset --hard HEAD~1
```