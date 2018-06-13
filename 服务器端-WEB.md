WEB资源分为静态和动态

静态：html
动态：JSP、Servlet、ASP、PHP

1.Tomcat
   tomcat/conf/servlet.xml 中设置

2.web.xml配置

3.浏览器把网站网址在Window的Host中是否知道网址IP，不知道再去找DNS中解析得到网址对应ip，通过IP网址转到相应网址
     （Host:window/system32/drivers/etc/hosts）


4.web资源访问图
    客户机机浏览器访问网站：1.询问本机window中host得到网址IP
                          2.没有从host中得到的话就会再从DNS找IP
                          3.得到IP后连接网站服务器端
                          4.连接后发送http请求
                          5.服务器从http请求中得到客户机想要访问的主机名以及想访问的应用和资源
                          6.从而读取相应主机的web应用和web资源  （得到html）
                          7.读取资源并回应http响应到服务器端
                          8.服务器端发送http响应至浏览器
                          9.浏览器解析响应
                          
   ![](https://github.com/StingLon/WEB-/blob/master/web%E8%B5%84%E6%BA%90%E8%AE%BF%E9%97%AE1.png)
   ![](https://github.com/StingLon/WEB-/blob/master/web%E8%B5%84%E6%BA%90%E8%AE%BF%E9%97%AE2.png)

（重点）5.HTTP协议          

   (1)http  ：超文本传输协议， 是TCP/IP协议的一个应用层协议，用于定义客户端与web服务器通讯的过程  
  
   (2)http请求
     请求行  （GET是默认方式，加?会在连接上显示，但get方式带的容量有限，而post方式无限量）
     请求头
     空行
     请求数据

    ！[](https://github.com/StingLon/WEB-/blob/master/%E5%93%8D%E5%BA%94.png)










































