# HTTP
HTTP (hypertext transport protocol) 协议 『超文本传输协议』,协议详细规定了浏览器和万维网服务器之间互相通信的原则。

## 请求报文 浏览器给服务器发送内容
```
行      1.请求类型: GET/POST 
        2.路径: URL /s?ie=utf-8 
        3.协议版本: HTTP/1.1
头      Host: atguigu.com
        Cookie: name=guigu
        Content-type: application/x-www-form-urlencoded
        User-Agent: chrome 83
空行
体      GET请求: 该内容为空
        POST请求: 该内容不为空 username=admin&password=admin

```

## 响应报文 服务器给浏览器返回结果
```
行      1.协议版本: HTTP/1.1 
        2.响应状态码: 200 
        3.响应状态字符串: OK
头      Content-Type: text/html;charset=utf-8
        Content-length: 2048
        Content-encoding: gzip
空行
体      <html>
            <head>
            </head>
            <body>
                <h1>尚硅谷</h1>
            </body>
        </html>

```

* 200     OK                      请求成功。一般用于 GET 与 POST 请求
* 201     Created                 已创建。成功请求并创建了新的资源
* 401     Unauthorized            未授权/请求要求用户的身份认证
* 404     Not Found               服务器无法根据客户端的请求找到资源
* 500     Internal Server Error   服务器内部错误，无法完成请求