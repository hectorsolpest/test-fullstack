## Ejemplo de formulario

- Crear el formulario
```console
php bin/console make:form UserType User
```

- Configurar UserType
```php
class UserType extends AbstractType
{
    public function buildForm(FormBuilderInterface $builder, array $options)
    {
        $builder
            ->add('username')
            ->add('email');
    }

    public function configureOptions(OptionsResolver $resolver)
    {
        $resolver->setDefaults([
            'data_class' => User::class,
        ]);
    }
}
```

- Crear el controlador
```php
class UserController extends AbstractController
{
    public function new(Request $request): Response
    {
        $user = new User();
        $form = $this->createForm(UserType::class, $user);

        $form->handleRequest($request);
        if ($form->isSubmitted() && $form->isValid()) {
            $entityManager = $this->getDoctrine()->getManager();
            $entityManager->persist($user);
            $entityManager->flush();

            return $this->redirectToRoute('user_success');
        }

        return $this->render('user/new.html.twig', [
            'form' => $form->createView(),
        ]);
    }
}
```

- Crear la vista

```twig
{% extends 'base.html.twig' %}

{% block body %}
    <h1>Crear Usuario</h1>

    {{ form_start(form) }}
        {{ form_widget(form) }}
        <button class="btn">Registrar</button>
    {{ form_end(form) }}
{% endblock %}
```