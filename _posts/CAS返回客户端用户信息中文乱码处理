---
layout: post
title:  CAS返回客户端用户信息中文乱码处理
date:   2018-07-24 14:50:00 +0800
categories: 后端技术
tag: [单点登录,CAS]

---
## 解决方案

客户端web.xml中配置
--
```
 <filter>
        <filter-name>ticketValidationFilter</filter-name>
        <filter-class>org.jasig.cas.client.validation.Cas20ProxyReceivingTicketValidationFilter
        </filter-class>
        <init-param>
            <param-name>casServerUrlPrefix</param-name>
            <param-value>http://localhost:8080/cas</param-value>
        </init-param>
        <init-param>
            <param-name>serverName</param-name>
            <param-value>http://localhost:8080/casClient2</param-value>
        </init-param>
        <!--中文乱码解决-->
        <init-param>
            <param-name>encoding</param-name>
            <param-value>UTF-8</param-value>
        </init-param>
    </filter>
```
