# ES6转es5


## 第一次安装
1. 在项目中创建 dist目录与src目录.
2. 确认装好nodejs,在根目录执行: npm init -y 命令来创建 package.json 文件.或 npm init 然后按需填写..下一步...下一步.....到完成.
3. 在项目根目录运行: D:\phpStudy\WWW\es6_es5>npm i babel-cli babel-core babel-polyfill babel-preset-env -D   来安装这几个插件
4. 在项目根目录创建 .babelrc 文件.内容:
```	
{
    "presets": [
      "env"
    ]
}
```

5. 修改package.json文件.在scripts属性中,增加两行内容,整个文件全附上.
```
{
  "name": "es6_es5",
  "version": "1.0.0",
  "description": "es6自动转成es5简单方法.",
  "main": "index.js",
  "scripts": {
    "build": "babel src -d dist",
    "watch": "babel src -d dist -w"
  },
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "babel-cli": "^6.26.0",
    "babel-core": "^6.26.3",
    "babel-polyfill": "^6.26.0",
    "babel-preset-env": "^1.7.0"
  }
}
```
6. 第四步那个配置文件可以不要,在package.json文件中增加一个  "babel" 属性也是可以的.内容如下:
```
{
  "name": "es6_es5",
  "version": "1.0.0",
  "description": "es6自动转成es5简单方法.",
  "main": "index.js",
  "scripts": {
    "build": "babel src -d dist",
    "watch": "babel src -d dist -w"
  },
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "babel-cli": "^6.26.0",
    "babel-core": "^6.26.3",
    "babel-polyfill": "^6.26.0",
    "babel-preset-env": "^1.7.0"
  },
  "babel": {
    "presets": [
      "es2015"
    ]
  }
}
```


## 操作
1. 执行install.bat 或   在根目录执行  npm i 来安装包.
2. 执行build.bat 或 npm run build, 把src目录中的es6写的js文件转成es5后保存到dist目录中.
3. 执行watch.bat 或 npm run watch, 开启自动监听src目录中的文件变动.