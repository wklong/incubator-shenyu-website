---
title: 数据库设计
keywords: db
description: 数据库设计
---

* 插件采用数据库设计，来存储插件，选择器，规则配置数据，以及对应关系。
* 数据库表 UML 类图:

 ![](/img/shenyu/db/shenyu-db.png)

* 设计详解:
  
   * 一个插件对应多个选择器，一个选择器对应多个规则。

   * 一个选择器对应多个匹配条件，一个规则对应多个匹配条件。

   * 每个规则在对应插件下，不同的处理表现为 handle 字段，handle 字段就是一个 json 字符串。具体的可以在 admin 使用过程中进行查看。
     
   * 资源权限设计用来存储用户名称、角色、资源数据以及对应关系。
   
* 数据库UML类图：

![](/img/shenyu/db/shenyu-permission-db.png)

* 设计详情:
   * 一个用户对应多个角色,一个角色对应多个资源。