# Scope
- Starting a Vue Project with Vue CLI 3
- Understanding how to communicate between parent and children components
- First touch with VUE Directives

## Initialization of a vue project
Run in command line
```
vue create <projectname>
```
Select ` default (babel, eslint) ` since the very project wont need any other features such as `vue router`

## Projectstructure

```
├── index.html
├── public
│   └── favicon.ico
│   └── index.html
├── src
│   └── APP.vue
│   └── components
│         └── Searchbar.vue
│         └── VideoDetail.vue
│         └── VideoList.vue
│         └── VideoListItem.vue
├── main.js
├── package.json
└── vue.config.js
```
### main.js
```
import Vue from 'vue'
import App from './App'

new Vue ({
    // el: '#app',
    render : h => h(App)
}).$mount('#app')
```
Inside the main.js file a new vue instance is being create. Since we want to render our Application, we are import it and mount it to the very root `<div>` which has the `id="app"` inside the `index.html` file.

Another way of rendering the Application:
```
new Vue ({
    render: function(createELement) {
        createElement(App) }
        }
```



# How to start the Project

## Development Build
```
npm install
npm run serve
```

### Production Build
```
docker build . -t <YOUR_IMAGE_NAME>
docker run -it -p 3000:80 <YOUR_IMAGE_NAME>
```



### Lints and fixes files
```
npm run lint
```

