ref: 
https://nodesource.com/blog/your-first-nodejs-package/
https://medium.com/@jdaudier/how-to-create-and-publish-your-first-node-js-module-444e7585b738#.u6uaujwwg

# CREAR MODULO NPM


## 1 - init

```
npm init
``

## 2 - index.js

```
module.exports = function(width, height) {  
  return width * height;
};
```

## 3 - login npm

```
npm login
```


## 4 - git

```
git add package.json index.js
git commit -m "preparar v1.0.0"
npm version 1.0.0
git push && git push --tags

```

## 5 - publish

Default is private (it's paid)
```
npm publish
```

Otherwise set public
```
npm publish --access=public
```

## versions

```
v0.0.0
breaking - feature - patch / bugs
```

## setting dependencies minimun version

*package.json*
```
"engines": {
  "node": ">=4.2.4"
},
```

## Cheat-Sheet
```
-D = --save-dev
-S = --save
```

