---
title: JSStudyTest
excerpt: page for js
tag: test
categories: 
- 博客测试
---

```
'use strict';
var http = require("http");

http.createServer(function (request,response){
    response.writeHead(200,{'Content-Type':'text/plain'});

    response.end('NMSL\n');
}).listen(8888);

let x=100;

console.log(x);

var o=[1,2,3,4,5];
for (var key in o) {
    console.log(key); 
}


for (var key of o) {
    console.log(key); 
}

var a=JSON.stringify(o);

console.log(o);

var fs = require('fs');

//异步
fs.readFile('./sample.txt','utf-8',function(err,data){
    if(err){
        console.log(err);
    }else{
        console.log(data);
    }
});

var data='NMSL';

fs.writeFile('output.txt',data,function(err){
    if(err){
        console.log(err);
    }else{
        console.log('ok');
    }
});
```