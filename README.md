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

