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

