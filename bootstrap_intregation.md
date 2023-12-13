## VUE.js with laravel Bootstrap Intregation 

### Step 1 : install bootstrap in the project of vue with laravel.

```
npm install bootstrap
npm install bootstrap-vue

```

### Step 2 : Then, open the main.js/app.js file on resource folder with your code editor. Import bootstrap

```
import { createApp } from 'vue'
import App from './App.vue'
import 'bootstrap/dist/css/bootstrap.css' // import this file
import 'bootstrap-vue/dist/bootstrap-vue.css' // import this file
createApp(App).mount('#app')

```

### Step 3 : Now run the project. Use the following command to run the project.

```
npm run dev

```

> Go to the following link http://127.0.0.1:8000/ and you will find the following
