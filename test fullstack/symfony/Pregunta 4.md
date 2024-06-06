### Creación del servicio

```php
class CalculatorService
{
    public function add($a, $b)
    {
        return $a + $b;
    }
}
```

### Registro del servicio

```yaml
services:
    App\Service\CalculatorService: ~
```

### Inyección del servicio

```php
class MathController
{
    private $calculator;

    public function __construct(CalculatorService $calculator)
    {
        $this->calculator = $calculator;
    }

    public function add($a, $b)
    {
        $result = $this->calculator->add($a, $b);
        return new Response("La suma de $a y $b es: $result");
    }
}

```

### Test unitario del servicio

```php
class CalculatorServiceTest extends TestCase
{
    public function testAdd()
    {
        $calculator = new CalculatorService();
        $result = $calculator->add(10, 15);

        $this->assertEquals(25, $result);
    }
}
```