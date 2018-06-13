Servlet

一种开发动态web资源的技术

运行流程：
        1.浏览器发送http请求到服务器端
        2.服务器端创建准备好request(请求头、请求体)、response（响应头、响应体）
        3.同时首次访问时创建servlet  并调用service方法传递执行request和response
        4.servlet的service方法执行后 向response写入响应信息
        5.服务端发现respnse信息中后读取发出http响应给浏览器













































