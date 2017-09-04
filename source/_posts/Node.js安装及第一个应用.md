---
title: Node.js安装及第一个应用
date: 2017-09-03 00:06:13
tags:
---
# Node.js 安装配置
Node.js安装包及源码下载地址为：<https://nodejs.org/en/download/>，可以根据自己不同的平台安装Node.js。

同时，Node.js的历史版本下载为：<https://nodejs.org/dist/>。
## 版本测试
	MacPro:blog Jing$ node --version
	v6.3.1
# Node.js 创建第一个应用
如果我们使用PHP来编写后端的代码时，需要Apache 或者 Nginx 的HTTP 服务器，并配上 mod_php5 模块和php-cgi。

从这个角度看，整个"接收 HTTP 请求并提供 Web 页面"的需求根本不需 要 PHP 来处理。

不过对 Node.js 来说，概念完全不一样了。使用 Node.js 时，我们不仅仅 在实现一个应用，同时还实现了整个 HTTP 服务器。事实上，我们的 Web 应用以及对应的 Web 服务器基本上是一样的。
在我们创建 Node.js 第一个 "Hello, World!" 应用前，让我们先了解下 Node.js 应用是由哪几部分组成的：

在我们创建 Node.js 第一个 "Hello, World!" 应用前，让我们先了解下 Node.js 应用是由哪几部分组成的：

1. 引入 required 模块：我们可以使用 require 指令来载入 Node.js 模块。
2. 创建服务器：服务器可以监听客户端的请求，类似于 Apache 、Nginx 等 HTTP 服务器。
3. 接收请求与响应请求 服务器很容易创建，客户端可以使用浏览器或终端发送 HTTP 请求，服务器接收请求后返回响应数据。
------

	var http= require("http");

	http.createServer(function (request,response) {
	// body...
	response.writeHead(200,{'Content-Type':'text/	plain'});

	response.end('hello world\n');

	}).listen(8888);

	console.log('Server running at http://	127.0.0.1:8888/');
	
