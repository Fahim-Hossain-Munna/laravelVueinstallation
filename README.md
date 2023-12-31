## How To Install Vue 3 In Laravel 10 With Vite

> [!TIP]
What is Laravel
> Laravel is a web application framework with expressive, elegant syntax.
> A web framework provides a structure and starting point for creating your application, allowing you to focus on creating something amazing while you sweat the details.

> [!IMPORTANT]
What is Vue js!
> Vue is a JavaScript framework for building user interfaces.
> It builds on top of standard HTML, CSS, and JavaScript.
> It Helps you efficiently develop user interfaces, be they simple or complex.


### Step 1: Create New Laravel Project

```
composer create-project laravel/laravel laravel10-vue3
```

### Step 2: How To Install Vue 3 on Laravel 10

```
npm install
npm install vue@next vue-loader@next

```

### Step 3: Install Plugin Vue From Vite

```
npm i @vitejs/plugin-vue

```

### Step 4: Edit File vite.config.js

```

// vite.config.js
import { defineConfig } from 'vite';
import laravel from 'laravel-vite-plugin';
import vue from '@vitejs/plugin-vue'

export default defineConfig({
    plugins: [
        vue(),
        laravel({
            input: ['resources/css/app.css', 'resources/js/app.js'],
            refresh: true,
        }),
    ],
});

```

### Step 5: Edit File app.js Inside Folder resources/js

```

import {createApp} from 'vue'

import App from './App.vue'

createApp(App).mount("#app")

```

### Step 6: Create File app.blade.php Inside Folder resources/views

> Make sure to add the css file and javascript as shown and also the div with id=app

```

<!DOCTYPE html>
<html lang="{{ str_replace('_', '-', app()->getLocale()) }}">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <title>ًApplication</title>
        @vite('resources/css/app.css')
    </head>
    <body>
        <div id="app"></div>
        @vite('resources/js/app.js')
    </body>
</html>

```

### Step 7: Create File App.vue Inside Folder resources/js

```

<template>
    <h1>
        How To Install Vue 3 in Laravel 10 : Laravel SPA.
    </h1>
</template>

```

### Step 8: Edit File web.php Inside Folder routes

```

use Illuminate\Support\Facades\Route;

Route::get('/', function () {
    return view('app');
})
->name('application');

```

### Step 9: Run PHP Local Server

```
php artisan serve

```

### Step 10: Run Node Local Server

```

npm run dev

```


> Go to the following link http://127.0.0.1:8000/ and you will find the following
