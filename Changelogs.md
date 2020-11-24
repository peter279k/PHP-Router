### v2.1.0
Some improvements:

- Changed namespace and directory structure. You must use `Buki\Router\Router` class instead of `Buki\Router` in order to create new Router instance. Please check documentation for more.
- The same middleware has been prevented from running twice.

### v2.0.0

A lot of updates and code optimization has been made for PHP-Router and released v2.0.0. For this version:

- Added and enhanced Request and Response support by using `symfony/http-foundation` package.
- Middleware usage was enhanced.
- Added base Controller and Middleware classes.
- Changed minimum PHP version as `^7.2.5`.
- Code optimizations...
