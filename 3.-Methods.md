PHP Router supports GET, POST, PUT, DELETE, OPTIONS, PATCH, HEAD, AJAX and ANY request methods.

## Usage 

```php
# GET Request
$router->get('/get-request', function()
{
  echo 'Hello World.';
});
```
```php
# POST Request
$router->post('/post-request', function()
{
  echo 'Hello World.';
});
```
```php
# PUT Request
$router->put('/put-request', function()
{
  echo 'Hello World.';
});
```
```php
# DELETE Request
$router->delete('/delete-request', function()
{
  echo 'Hello World.';
});
```
```php
# AJAX Request
$router->ajax('/ajax-request', function()
{
  echo 'Hello World.';
});
```
```php
# AJAXP Request (Post & Ajax)
$router->ajaxp('/ajaxp-request', function()
{
  echo 'Hello World.';
});
```
```php
# ANY Request (It accepts all requests.)
$router->any('/any-request', function()
{
  echo 'Hello World.';
});
```

You can define more than one method at one time for a request.

Example:
```php
$router->add('GET|POST', '/request', function()
{
  echo "Hello World. I'm working GET or POST method.";
});
```

**NOTE:**

A post value must be sent in an object named **"_method"** for the Put, Delete, Patch, Options, Head methods.

Example: 
```php
# curl -X PUT http://localhost:3000/put-request
# OR 
# curl -X POST http://localhost:3000/put-request -d _method=put

$router->put('/put-request', function()
{
  echo 'Hello World.';
});
```