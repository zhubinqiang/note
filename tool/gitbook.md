# gitbook
[TOC]

gitbook 是 git + markdown 写作工具, 它由nodejs编写，安装的时候需要先安装nodejs环境和npm

## 安装
```sh
npm install gitbook-cli -g
```

## 初始化
`gitbook init` 在当前目录下会生成 README.md 和 SUMMARY.md 2个文件

其中 README.md 是首页的介绍

SUMMARY.md 是gitbook的目录结构
```md
# Summary

* [Introduction](README.md)
* [tool](tool/README.md)
    * [gitbook](tool/gitbook.md)
```

## 生成静态网页
`gitbook build` 在当前目录下生成一个 _book 的目录

## 启动服务
`gitbook serve` 会启动一个http服务 在浏览器中访问 http://localhost:4000

## 插件
在根目录下新建一个 book.json 的文件
```js
{
    "language": "zh-hans",
    "plugins": [
        "search-pro"
    ]
}
```

安装插件
```sh
gitbook install -g search-pro
```

也可以通过npm去安装
```sh
npm install gitbook-plugin-toc -g
```