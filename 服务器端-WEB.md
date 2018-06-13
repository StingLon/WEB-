WEB资源分为静态和动态

静态：html
动态：JSP、Servlet、ASP、PHP

1.Tomcat
   tomcat/conf/servlet.xml 中设置



2.web.xml配置

3.浏览器把网站网址在Window的Host中是否知道网址IP，不知道再去找DNS中解析得到网址对应ip，通过IP网址转到相应网址
     （Host:window/system32/drivers/etc/hosts）


4.web资源访问图
    例如查询   http://www.baidu.com.cn/mail/1.html
                           ↓
                           ↓
   windows.hosts文件   ←1. ←ie
                           ↓
          dns服务器    ←2.← ↓
   ![](https://github.com/StingLon/WEB-/blob/master/web%E8%B5%84%E6%BA%90%E8%AE%BF%E9%97%AE1.png)
