# Resource Controllers

"CRUD" opreation is a  common case. CRUD opreation for all model makes web.php file unnessary large  we can replace this using Resource Controllers. Laravel resource routing assigns the typical create, read,
update, and delete ("CRUD") routes to a controller with a single line of code

To get started, we can use the make:controller Artisan command's --resource option to quickly create a controller to handle these actions
```
 php artisan make:controller PhotoController --resource
```

```php
use App\Http\Controllers\PhotoController;
Route::resource('photos', PhotoController::class);
```

we can also write multiple resource controllers at once by passing an array to the resources method:
```php
Route::resources([
    'photos' => PhotoController::class,
    'posts' => PostController::class,
])
```


