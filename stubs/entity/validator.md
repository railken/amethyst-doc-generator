## {{ data.components.validator }}

The validator is used during any operation that manipulate the data to check if the parameters are correct. Remember that each attribute has is own validation.

#### Extend the class

Create the new validator in `app/Validators/{{ data.className }}Validator`
```php
namespace App\Validators;

use {{ data.components.validator }} as Validator;

class {{ data.className }}Validator extends Validator {
	// ...
}
```
Update the file `configs/amethyst.{{data.package}}` with the new class
```php
return [
    'data' => [
        '{{ data.name }}' => [
            'validator' => App\Validators\{{ data.className}}Validator::class,
        ],
    ]
];
```

---
[Back](index.md)