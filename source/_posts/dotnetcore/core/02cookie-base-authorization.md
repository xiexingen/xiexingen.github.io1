---
title: 基于CookieBase认证的模式
author: 谢新根
categories:
  - .NetCore
tags:
  - .NetCore
abbrlink: 31048
date: 2018-03-05 21:01:01
---

基于CookieBase认证的模式
<!-- more -->

>说明 通过vs2017新建的.net core项目默认没有添加身份认证与授权以及路由等  
1. 在StartUp.ConfigureServices中addMvc之前添加AddAuthentication  
using Microsoft.AspNetCore.Authentication.Cookies;
![](https://cdn.jsdelivr.net/gh/xiexingen/blog/assets/images/dotnetcore/core/02/0101.png)
2. 在Configure方法中  
![](https://cdn.jsdelivr.net/gh/xiexingen/blog/assets/images/dotnetcore/core/02/0201.png)
3. 模拟登陆  
using Microsoft.AspNetCore.Authentication;
using Microsoft.AspNetCore.Authentication.Cookies;
using System.Security.Claims;
![](https://cdn.jsdelivr.net/gh/xiexingen/blog/assets/images/dotnetcore/core/02/0301.png)
4. 在对应的Controller或者Action中贴上属性[Authorize]  