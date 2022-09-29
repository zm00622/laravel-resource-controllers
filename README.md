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
To see the routes are successfully created in your view in the browser, simply add ```return 'index';``` to the index function in your controller. You can repeat this for each function in the controller, and then navigate to those routes.

Next, you are going to want to add the views to your resources > views folder. For this, we recommend using a template. 

After the views are added, you are going to want to run the following commands (where posts is the name of the db table):

```
php artisan make:migration create_posts_table

```

Lastly, migrate your table:

```
php artisan migrate

```