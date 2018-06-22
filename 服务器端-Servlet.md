Servlet  以及相关API （servletConfig、servletContext）

Servlet 是指任何实现了这个Servlet接口的类，由服务器调用的，运行在服务器端。

一种开发动态web资源的技术
作用：
Servlet能够处理浏览器带来HTTP请求，并返回一个响应给浏览器，从而实现浏览器和服务器的交互。

为什么Servlet是单例的
浏览器多次对Servlet的请求，一般情况下，服务器只创建一个Servlet对象，也就是说，Servlet对象一旦创建了，就会驻留在内存中，为后续的请求做服务，直到服务器关闭。

1.运行过程：
        1.浏览器发送http请求到服务器端
        2.服务器端创建准备好request(请求头、请求体)、response（响应头、响应体）
        3.同时首次访问时创建servlet  并调用service方法传递执行request和response
        4.servlet的service方法执行后 向response写入响应信息
        5.服务端发现respnse信息中后读取发出http响应给浏览器
  生命周期：
        1.Servlet 第一访问创建实例，通过调用 init () 方法进行初始化。
        2.Servlet 调用 service() 方法来处理客户端的请求。
        3.Servlet 通过调用 destroy() 方法终止（结束）。
        4.最后，Servlet 是由服务器停止或移除的时候进行垃圾回收的
        
        
2.servlet接口 默认的两个实现类分别为 GenericServlet、HttpServlet
      因为httpServlet实现servlet接口时覆写了service方法，所以只需覆写doGet、doPost方法  

3.HttpServlet
     doGet、doPost
     
4.线程安全
    同步线程可行但不方便，因此使用接口SingleThreadMode方式 ，不能抛异常，只能try-catch
    
   线程安全问题
当多个用户访问Servlet的时候，服务器会为每个用户创建一个线程。当多个用户并发访问Servlet共享资源的时候就会出现线程安全问题。


5.web.XML配置
例如：
   <servlet-name>ServletDemo1</servlet-name>
    <servlet-class>web1.ServletDemo1</servlet-class>
  </servlet>
  <servlet-mapping>
    <servlet-name>ServletDemo1</servlet-name>
    <url-pattern>/*</url-pattern>
  </servlet-mapping>





////
Servlet其中的API:servletConfig、servletContext


1.servletConfig  
  作用： 用于封装servlet的配置信息,通过此对象可以读取web.xml中配置的初始化参数。
  
2.servletContext
  servletContext对象通常称为context域对象，  全局域对象            代表着当前web站点


  servletContex的方法  ：  ServletContext context= this.getServletContext();
 
 作用：ServletContext可以获取的是配置整个web站点的参数信息
       所有Servlet都共享着一个ServletContext对象，所以Servlet之间可以通过ServletContext实现通讯。
       实现servlet的转发
       利用servletContext对象读取资源文件
  
 
 
 
 实现Servlet之间通讯就要用到ServletContext的setAttribute(String name,Object obj)方法
 
 
 
 
 
 
 properties文件读取
   












































