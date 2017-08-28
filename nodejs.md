# Node.js #
---
Node.js 是一个基于 Chrome V8 引擎的 JavaScript 运行环境。
Node.js 使用了一个事件驱动、非阻塞式 I/O （异步）的模型，使其轻量又高效。
Node.js 的包管理器 npm，是全球最大的开源库生态系统。

简单的说 Node.js 就是运行在服务端的 JavaScript。

Node.js 是谷歌 V8 引擎、libuv平台抽象层 以及主体使用 Javscript 编写的核心库三者集合的一个包装外壳。（注：V8是谷歌开发的，目前公认最快的 Javascript 解析引擎，libuv 是一个开源的、为 Node 定制而生的跨平台的异步 IO 库）

**特征：**
1. 单线程
2. 单个事件驱动
3. 非阻塞式IO（异步IO），高性能

**运行：**
node 文件名


**搭建服务器**
```
const http = request('http');
const server = http.createServer(function(request,response){
  request.url  可以拿到前端的信息
  response.write('write')  给前端发送信息
  response.end();
})
```

**writeFile(文件名,'内容',回调(error))   写文件**
```
fs.writeFile('2.txt','我是222',(error) => {
  if(error){
    console.log('error');
  }
  console.log('finish');
})
```

**删除文件**
```
//1.异步  fs.unlink('文件名',回调)
fs.unlink('2.txt',() => {
  console.log('delect finish');
})

//2.同步
fs.unlinkSync('2.txt');
console.log('delect finish');
```
