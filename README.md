# 一，搭建迷你服务器

## 1，创建一个文件夹为mini_server

## 2,  win+r打开cmd命令，

```powershell
cd mini_server路径
```

## 3，加载npm

```powershell
npm init
package name mini_server
```

## 4，安装express

```powershell
npm i express
```

## 5，安装路由的history

```powershell
npm i connect-history-api-fallback
```

## 6，在mini_server文件下创建一个server.js文件完成以下配置

server.js

```js
// npm init
// package name mini_server
// npm i express
// npm i connect-history-api-fallback
//微型服务配置
const express = require('express');
const history = require('connect-history-api-fallback');

//创建应用
const app = express();

//修复history把路由当请求接口的异常
app.use(history());
//应用指向到文件夹
app.use(express.static(__dirname+'/static'));

//启动
app.listen(80,(err)=>{
    if(!err){
        console.log("服务器启动成功");
    }
})
```

##7，在vs-code工具里输入以下命令

![捕获](E:\Desktop\Vue\VueWorkSpace\19\node server.PNG)

# 二，部署项目到服务器

## 1，将要部署的项目打包成dist文件将里面的static和index.html文件拷贝到mini_serserver 的static文件下

## 2，打开服务器

## 3，启动服务器
![node server](images/node%20server.PNG)

## 4，通过公网ip访问