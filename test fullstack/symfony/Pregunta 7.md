### Ejemplo de consulta en doctrine

```php
class ProductRepository extends ServiceEntityRepository
{
    public function __construct(ManagerRegistry $registry)
    {
        parent::__construct($registry, Product::class);
    }

    public function findProductsExpensiveThan100()
    {
        return $this->createQueryBuilder('p')
            ->andWhere('p.price > :price')
            ->setParameter('price', 100)
            ->getQuery()
            ->getResult();
    }
}

```