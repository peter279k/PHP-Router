The patterns defined in PHP-Router are:


- {a} => All chars without '/' char. 
- {d} => Digits. 
- {i} => Digits. 
- {s} => Alphabetic characters. 
- {w} => Alphanumeric characters. 
- {u} => URL format characters for SEO. (Alphanumeric characters, _ and -) 
- {*} => All characters


### single pattern
```php
# get request -> localhost/hello/{s}
$router->get('/hello/{s}', function($value)
{
  echo 'Hello, ' . $value;
});

# Output:
# /hello/burak ---> Hello, burak
# /hello/php ---> Hello, php
# /hello/ ---> Error!!!
```

### multi pattern
```php
# get request -> localhost/post/{i}/{u}
$router->get('/post/{i}/{u}', function($id, $slug)
{
  echo "Post ID: " . $id . "<br />";
  echo "Post Slug: " . $slug;
});

# Output:
# /post/5/hello-world ---> Post ID: 5 <br />Post Slug: hello-world
# /post/17/php-router ---> Post ID: 17 <br />Post Slug: php-router
# /post/foo/bar ---> Error!!! ({i} params cannot be string.)
```

### optional pattern - add default value
```php
# get request -> localhost/page/{u}
$router->get('/page/{u?}', function($page = 'home')
{
  echo "Page: " . $page;
});

# Output:
# /page/contact ---> Page: contact
# /page/about-us ---> Page: about-us
# /page ---> Page: home
```

### custom pattern - create own pattern
```php
$router->pattern('lowercase', '[a-z]+');

$router->get('/demo/{lowercase}', function($value)
{
  echo "Value: " . $value;
});

# Output:
# /demo/burak ---> Value: burak 
# /demo/php ---> Value: php
# /demo/Router ---> Error!!!
```
To define multiple patterns at once, you can use this method:
```php
$patterns = ['lowcase' => '[a-z]+', 'upcase' => '[A-Z]+'];

$router->pattern($patterns);
```
Great! That's it. :)


