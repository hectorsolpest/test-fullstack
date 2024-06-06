## Inyección de depencias en symfony

La Inyección de Dependencias (DI) es un patrón de diseño utilizado en Symfony y otros frameworks modernos para gestionar las dependencias entre clases. El objetivo principal de DI es reducir el acoplamiento entre clases y aumentar la modularidad y la facilidad de prueba del código.

En Symfony, DI se implementa a través del Contenedor de Servicios, que es una herramienta poderosa que crea y gestiona los servicios de tu aplicación. Un servicio es simplemente un objeto que realiza una tarea específica, como enviar un correo electrónico o manejar una carga de archivos.

- Ejemplo de servicio

```yaml
services:
    App\Service\MyService:
        arguments:
            $myDependency: '@App\Service\MyDependency'
```

- Ejemplo de Inyección de depencias

```php
class MyService
{
    private $myDependency;

    public function __construct(MyDependency $myDependency)
    {
        $this->myDependency = $myDependency;
    }
}
```