### Faker Password Provider for Hautelook AliceBundle

Install the package:

`composer req colvin/faker-password-provider --dev`

Define the service in `services.yaml`:

```
services:
    Colvin\Faker\Provider\PasswordProvider:
        tags: ['hautelook_alice.faker.provider']
```

You can now use the `encodePassword` formatter in your fixtures:

```
App\Entity\User:
    user:
        password: <encodePassword(@user, 'test')>
        username: test
        roles: ['ROLE_USER']
``` 