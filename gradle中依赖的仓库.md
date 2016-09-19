# Gradle中依赖的仓库

# 仓库是什么?

顾名思义,仓库就存放东西的. 放什么东西呢？ 简单来说就是存放我们依赖的jar包.

## 

Gradle支持哪些仓库?

* Maven仓库
* Ivy仓库
* 平级目录仓库

## 如何在构建中加入这些仓库?

Ivy仓库应该用的人不多吧,这里就不多作介绍了,重点放在maven仓库上.

在build.gradle中添加仓库的声明,方法如下:

从Maven仓库中获取依赖

## Maven仓库的三种别名

为了更加方便的加入Maven仓库, Gradle为我们提供了3种别名,分别是:

### 1.mavenCentral\(\)：

表示从maven中央仓库中获取依赖 地址: http:\/\/repo1.maven.org\/maven2

### 2.jcenter\(\):

jcenter是一个新的远程中央仓库，兼容maven中央仓库，而且性能更优.

gradle默认使用jcenter作为仓库.

jcenter存放在这里:https:\/\/bintray.com\/

### 3.mavenLocal\(\):

表示从本地Maven仓库中获取依赖。 本地地址: {user.home}\/.m2\/repository

从平级目录仓库中获取依赖

从本地目录中获取依赖,在build.gradle中添加:

