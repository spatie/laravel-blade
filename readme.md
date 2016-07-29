# Use Laravel's blade outside Laravel

[![Latest Version on Packagist](https://img.shields.io/packagist/v/spatie/laravel-blade.svg?style=flat-square)](https://packagist.org/packages/spatie/laravel-blade)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)

### Installation
The package can be installed via Composer by requiring the "50onred/laravel-blade": "1.3" package in your project's composer.json.

```bash
composer require spatie/laravel-blade
```

## Postcardware

You're free to use this package (it's [MIT-licensed](LICENSE.md)), but if it makes it to your production environment you are required to send us a postcard from your hometown, mentioning which of our package(s) you are using.

Our address is: Spatie, Samberstraat 69D, 2060 Antwerp, Belgium.

The best postcards will get published on the open source page on our website.

### Usage

```php
<?php

/*
|--------------------------------------------------------------------------
| Register The Auto Loader
|--------------------------------------------------------------------------
|
| Composer provides a convenient, automatically generated class loader
| for our application. We just need to utilize it! We'll require it
| into the script here so that we do not have to worry about the
| loading of any our classes "manually". Feels great to relax.
|
*/

require 'vendor/autoload.php';

use Spatie\Blade\Blade;

$views = __DIR__ . '/views';
$cache = __DIR__ . '/cache';

$blade = new Blade($views, $cache);
echo $blade->view()->make('hello');
```

You can use all blade features as described in the Laravel 4 documentation:
http://laravel.com/docs/templates#blade-templating
