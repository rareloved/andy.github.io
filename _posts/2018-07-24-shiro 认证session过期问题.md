---
layout: post
title:  shiro认证session过期问题
date:   2018-07-24 00:00:00 +0800
categories: 后端技术
tag: shiro

---

* content
{:toc}


##设置地方

1.tomcat 容器中 			{#tomcat}
------------------------------------

session-config

```
<session-config>
<session-timeout>30</session-timeout>
</session-config>
```

2.工程中web.xml配置        {#tomcat1}
------------------------------------
```
<session-config>
<session-timeout>30</session-timeout>
</session-config>
```
3.shiro spring配置文件

```
<!-- 会话管理器 -->
<bean id="sessionManager" class="org.apache.shiro.web.session.mgt.DefaultWebSessionManager">
    <!-- 设置超时时间 -->
    <property name="globalSessionTimeout" value="1800000"/>
</bean>
```