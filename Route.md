# Route in Laravel
---

All laravel route define in routes/web.php file. Or we Can say that  The routes/web.php file defines routes that are for your web interface. 

### Route code
```php
Route::get('/user', function () {
    return 'Hello user';
});
```
Here `/user` is url and the nezt part is call back function. In short from we can say 
```php
Route::get($uri, $callback);
```

### web.php vs api.php
Although web.php and api.php both are content route but there are sone diference and different purpose. And the differance are
- For all requests for normal web applications, we use web.php.
- For a mobile app (iOS, Android for example) define your routes in api.php.
- routes are using auth and api middleware, and api middleware adds some additional security/protection. So a client can request a route only x time per minute
- There is rate limiting configured for api routes.

In `app\Providers\RouteServiceProvider.php` we can see a block of code, That is limiting the access of user

``` php
 RateLimiter::for('api', function (Request $request) {
            return Limit::perMinute(60)->by($request->user()?->id ?: $request->ip());
    });
```






