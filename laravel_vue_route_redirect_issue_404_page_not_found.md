### You are getting 404 page because laravel couldn't find that route which you have declared in Vue.

+ On your laravel's web.php routes file, include this

``` laravel
Route::get('/{any}', function () {
    return view('app');
})->where('any', '.*');

```

> [!NOTE]
> In this way, you are telling to laravel that I will handle(vue) on my own.


> Go to the following link http://127.0.0.1:8000/ and you will find the following