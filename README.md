# Symfony forms for concrete5

This is a composer package that provides the possibility to use [Symfony forms](https://symfony.com/doc/current/book/forms.html)
within concrete5. The advantages are obvious if you have read anything about them but to list a few:

- Automatic form tags generation based on the defined fields
- Automatic CSRF validation
- Automatic field errors based on the defined validators
- Automatic saving of forms directly into Doctrine entities
- Less things to worry about in your controller logic
- Streamlining your development pipeline with single pages
- Making developing single page views with forms a lot faster
- Less bugs in your code due to the nature of generalized and well tested components

This package depends on the twig templates package for building the form views:

[https://github.com/mainio/c5pkg_twig_templates](https://github.com/mainio/c5pkg_twig_templates)

## How to use?

Add a composer.json file into your concrete5 package's directory. Into that
file, add the following content:

```
{
    "require": {
        "mainio/c5-symfony-forms": "*"
    }
}
```

And then run `composer install` in the same directory. After this, add the
following on top of your package controller (after the namespace definition):

```php
include(dirname(__FILE__) . '/vendor/autoload.php');
```

An example implementation on how to use this is available here:

[https://github.com/mainio/c5_symfony_forms_example](https://github.com/mainio/c5_symfony_forms_example)

In order to use this, you will need to be running PHP 5.4 or newer in order to take advantage of the
necessary trait provided by this package.

## License

Licensed under the MIT license. See LICENSE for more information.

Copyright (c) 2015 Mainio Tech Ltd.