### Controlador
```php
class HelloController
{
    public function index($name = 'World')
    {
        return new Response(sprintf('Hello %s!', htmlspecialchars($name)));
    }
}
```
### Test Unitario

```php

class HelloControllerTest extends WebTestCase
{
    public function testHelloName()
    {
        $client = static::createClient();
        $crawler = $client->request('GET', '/hello/John');

        $this->assertResponseIsSuccessful();
        $this->assertSelectorTextContains('body', 'Hello John!');
    }

    public function testHelloWorld()
    {
        $client = static::createClient();
        $crawler = $client->request('GET', '/hello');

        $this->assertResponseIsSuccessful();
        $this->assertSelectorTextContains('body', 'Hello World!');
    }
}

```