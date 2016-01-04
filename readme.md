### Installation
Install package composer "composer require eti/laravel-blade"

```json
{
	"require": {
	    "eti/laravel-blade": "^1.0"
	}
}
```


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

use ETI\BLADE\Blade;

$views = __DIR__ . '/app/views';
$cache = __DIR__ . '/cache';

$blade = new Blade($views, $cache);
echo $blade->view()->make('hello')->render();
```

You can use all blade features as described in the Laravel 5 documentation:
https://laravel.com/docs/5.1/blade