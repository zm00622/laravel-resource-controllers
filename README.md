# laravel-resource-controllers
This repo is boilerplate for a project with multiple resource controllers.

To see the source code for the YouTube tutorial, switch to branch lara-tut6.

```
composer create-project laravel/laravel name_of_your_project_directory
```

```
php artisan make:controller PostController --resource --model=Post
```

```
php artisan make:controller StudentController --resource --model=Student
```

paste into web.php

```
use App\Http\Controllers\PostController;
use App\Http\Controllers\StudentController;
Route::resource('products', PostController::class);
Route::resource('students', StudentController::class);
```

```
php artisan route:list
```
