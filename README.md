
tinylee's blog
====
blog基于[pelican](https://blog.getpelican.com/)构建，pelican是使用python编写的静态网站生成工具，支持使用Markdown、reStructuredText格式编写文章，还支持Disqus评论系统。

##安装
###virtualenv
- 建立Virtualenv虚拟环境
```shell
virtualenv blog
```
-  blog虚拟环境生效
```shell
cd blog
source ./bin/activate
```
- 安装pelican和依赖包
```shell
pip install pelican markdown fabric
```
- 生成项目
```shell
pelican-quickstart
```

##安装主题
- 列出已经安装的theme
```shell
pelican-themes -l
```
- 安装theme
```shell
pelican-themes -vi ./pelican-themes/zurb-F5-basic
```
- 删除theme
```shell
pelican-themes -vr zurb-F5-basic
```

##编写新文章
在**content**目录下新建markdown格式(.md)文件.

文章按下面模版编写：

```
Title: My super title
Date: 2010-12-03 10:20
Modified: 2010-12-05 19:30
Category: Python
Tags: pelican, publishing
Slug: my-super-post
Authors: Alexis Metaireau, Conan Doyle
Summary: Short version for index and feeds

This is the content of my super blog post.
```
##发布blog
blog发布使用工具：`fabric`

1. 首先构建blog
```shell
fab build
```

2. 在本地测试
```shell
fab serve
```

3. 发布blog
```shell
fab publish
```


##SCM
blog文章放在github进行备份管理：

    git@github.com:tinylee/blog.git

personal blog [http://tinylee.info](http://tinylee.info)
