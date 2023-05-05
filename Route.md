# Route in Laravel
---

All laravel route define in routes/web.php file. Or we Can say that  The routes/web.php file defines routes that are for your web interface. 

##### Route code
```php
Route::get('/user', function () {
    return 'Hello user';
});
```
Here `/user` is url and the nezt part is call back function. In short from we can say 
```php
Route::get($uri, $callback);
```



