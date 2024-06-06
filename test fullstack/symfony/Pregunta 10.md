## Creación de un Event Subscriber

- Crear la clase

```php
class RequestSubscriber implements EventSubscriberInterface
{
    private $logger;

    public function __construct(LoggerInterface $logger)
    {
        $this->logger = $logger;
    }

    public static function getSubscribedEvents()
    {
        return [
            RequestEvent::class => 'onKernelRequest',
        ];
    }

    public function onKernelRequest(RequestEvent $event)
    {
        $request = $event->getRequest();
        $this->logger->info('Nueva visita: ' . $request->getUri());
    }
}
```
- Configurar el servicio

```yaml
services:
    App\EventSubscriber\RequestSubscriber:
        arguments:
            $logger: '@logger'
        tags:
            - { name: 'kernel.event_subscriber' }

```

- Configurar el logger

```yaml
monolog:
    channels: ['request_log']
    handlers:
        request_log:
            type: stream
            path: '%kernel.logs_dir%/request.log'
            level: info
            channels: ['request_log']

```