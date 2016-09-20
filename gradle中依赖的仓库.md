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

```
repositories {


1.从指定的远程maven仓库中获取依赖

maven {

url "http://maven.helloword.net/repo"

}



2.从指定的本地maven仓库中获取依赖

maven {

url "file:///Users/bixiaopeng/mvn"

}



3.从中央Maven仓库中获取依赖

mavenCenter()



4.从新的中央远程仓库中获取依赖

jcenter()



5.从本地仓库中获取依赖

mavenLocal()



6.需要认证的库

maven {

credentials {

username 'user'

password 'password'

}

url "http://repo.helloword.com/maven2"

}

}

```
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

```
repositories {

//从当前项目的平级目录lib中获取依赖

    flatDir(dir: 'lib', name: 'libs directory')

//从当前项目的平级目录libA和libB中获取依赖

flatDir {

    dirs 'libA', 'libB'

    name = 'All dependency directories'

    }

}

```

