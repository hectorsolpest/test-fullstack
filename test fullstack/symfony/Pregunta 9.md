## Ejemplo de Validator

- Definir la restricción (Constraint)

```php
class ForbiddenDomain extends Constraint
{
    public $message = 'El dominio "{{ domain }}" no está permitido.';

    public $forbiddenDomain = 'example.com';
}
```

- Crear clase validator
```php
class ForbiddenDomainValidator extends ConstraintValidator
{
    public function validate($value, Constraint $constraint)
    {
        if (null === $value || '' === $value) {
            return;
        }

        $domain = substr(strrchr($value, "@"), 1);
        if ($domain === $constraint->forbiddenDomain) {
            $this->context->buildViolation($constraint->message)
                ->setParameter('{{ domain }}', $domain)
                ->addViolation();
        }
    }
}
```

- Configurar la validación en la entidad
```php
class User
{
    /**
     * @ORM\Column(type="string", length=180, unique=true)
     * @Assert\NotBlank
     * @Assert\Email
     * @ForbiddenDomain(forbiddenDomain="example.com")
     */
    private $email;
}
```