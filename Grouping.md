If you want you can group the routes you create.

Example:

```php
$route->group('admin', function()
{
  $route->get('foo', function(){ echo 'page: admin/foo'; });
  $route->get('bar', function(){ echo 'page: admin/bar'; });
  $route->get('baz/php', function(){ echo 'page: admin/baz/php'; });
  $route->post('login', function(){ echo 'page: admin/login'; });
});

# Created Routes:
/*
- GET /admin/foo
- GET /admin/bar
- GET /admin/baz/php
- POST /admin/login
*/
```