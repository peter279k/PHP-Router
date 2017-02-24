## Install
composer.json file:
```json
{
    "require": {
        "izniburak/router": "^1"
    }
}
```
after run the install command.
```
$ composer install
```
OR run the following command directly.
```
$ composer require izniburak/router
```

## Quick Usage
```php
require 'vendor/autoload.php';

$router = new \Buki\Router();

$router->get('/', function() {
    return 'Hello World!';
});

$router->run();
```

And add this code to the .htaccess file:

```php
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^ index.php [L]
```

Congratulations! Now, you can use PHP-Router.

If you have a problem, you can [contact me][support-url] or open new issue.

[support-url]: https://github.com/izniburak/php-router#support