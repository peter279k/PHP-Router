If you want you can group the routes you create.

Example:

```php
$router->group('admin', function($r)
{
  $r->get('foo', function(){ echo 'page: admin/foo'; });
  $r->get('bar', function(){ echo 'page: admin/bar'; });
  $r->get('baz/php', function(){ echo 'page: admin/baz/php'; });
  $r->post('login', function(){ echo 'page: admin/login'; });
});

# Created Routes:
/*
- GET /admin/foo
- GET /admin/bar
- GET /admin/baz/php
- POST /admin/login
*/
```