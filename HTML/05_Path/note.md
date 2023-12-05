# 路径的书写
用到路径的元素比较多，如：img、link、script、a、base等，规范的路径书写可以提高网站的访问速度和网页的兼容性，并且方便维护。

## 站内资源和站外资源
站内资源：当前网站的资源
站外资源：当前网站以外的资源

> 对站外资源使用绝对路径，对站外资源尽量使用相对路径

****

## 绝对路径
绝对路径的书写格式(url地址)：
```
协议名://主机名:端口号/路径
schema://host:port/path 
```
- 协议名的种类：http、https、ftp、file等
    - 如果当前站点和目标站点协议相同时，协议名可以省略(使用当前站点的协议)
- 主机名的种类：域名、IP地址（公网IP、局域网IP）
    - 如果当前站点和目标站点主机名相同时，主机名可以省略
- 端口号的种类：
    - 如果当前站点和目标站点端口号相同时，端口号可以省略
    - 如果协议是http，默认端口是80
    - 如果协议是https，默认端口是443
- 路径：每一种资源在网站上的路径是唯一的，即绝对路径，也是url地址内的路径

****

## 相对路径
|路径形式|对应含义|举例|
|:--:|:--:|:--:|
|`/`|表示根目录|`<a href="/index.html">`|
|`./`|表示当前目录|`<a href="./index.html">`|
|`../`|表示上一级目录|`<a href="../01_FirstWeb/index.html">`|
