Servlet  以及相关API （servletConfig、servletContext）

Servlet 是在服务器上运行的服务连接器

一种开发动态web资源的技术

1.运行过程：
        1.浏览器发送http请求到服务器端
        2.服务器端创建准备好request(请求头、请求体)、response（响应头、响应体）
        3.同时首次访问时创建servlet  并调用service方法传递执行request和response
        4.servlet的service方法执行后 向response写入响应信息
        5.服务端发现respnse信息中后读取发出http响应给浏览器
  生命周期：
        1.Servlet 通过调用 init () 方法进行初始化。
        2.Servlet 调用 service() 方法来处理客户端的请求。
        3.Servlet 通过调用 destroy() 方法终止（结束）。
        4.最后，Servlet 是由服务器停止或移除的时候进行垃圾回收的
        
        
2.servlet接口 默认的两个实现类分别为 GenericServlet、HttpServlet
      因为httpServlet实现servlet接口时覆写了service方法，所以只需覆写doGet、doPost方法  

3.HttpServlet
     doGet、doPost
     
4.线程安全
    同步线程可行但不方便，因此使用接口SingleThreadMode方式 ，不能抛异常，只能try-catch


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
  作用： 用于封装servlet的配置信息
  
2.servletContext
  servletContext对象通常称为context域对象

  servletContex的方法  ： context= this.getServletContext();
 
 作用：获取web应用的初始化参数
       实现servlet的转发
       利用servletContext对象读取资源文件
  
  properties文件读取
   












































