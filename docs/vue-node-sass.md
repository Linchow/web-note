# 解决node-sass下载失败的问题

安装node-sass依赖时总是会报没有安装Python或者node-sass安装失败的问题，原因是下载node-sass需要从国外网站下载文件，由于国内网络问题会因为下载超时而失败。
最简单的办法就是使用VPN下载或者使用淘宝镜像。

```
npm i node-sass --sass_binary_site=https://npm.taobao.org/mirrors/node-sass/

// 或者设置全局镜像源
npm config set sass_binary_site https://npm.taobao.org/mirrors/node-sass/
```