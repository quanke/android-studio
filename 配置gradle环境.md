# 配置Gradle环境

本文以Mac上配置Gradle环境为例进行介绍.
## 一. 下载gradle
1.1 下载地址: http://gradle.org/gradle-download/

1.2 下载最新版本:gradle-2.13 (当前最新版为2.13)

当然你也可以选择下载某一个历史版本,在页面右边Choose Vesion 中选择下载到本地后解压.二. 配置环境变量2.1 我的本地存放路径:/Volumes/warehouse/dev-tools/tools-jars/gradle-2.132.2 编缉.bash_profile： vim ~/.bash_profile2.3 配置环境变量:

```
export GRADLE_HOME=/Volumes/warehouse/dev-tools/tools-jars/gradle-2.13

export PATH=$PATH:$GRADLE_HOME/bin

```

2.3.使配置立即生效: source ~/.brash_profile

三. 查看配置是否成功

```
~$ gradle -v


------------------------------------------------------------

Gradle 2.13

------------------------------------------------------------


Build time: 2016-04-25 04:10:10 UTC

Build number: none

Revision: 3b427b1481e46232107303c90be7b05079b05b1c

Groovy: 2.4.4

Ant: Apache Ant(TM) version 1.9.6 compiled on June 29 2015

JVM: 1.8.0_91 (Oracle Corporation 25.91-b14)

OS: Mac OS X 10.11.2 x86_64

```

如果电脑上不单独配置Gradle环境也没关系, 因为Android Studio中使用了Gradle Wrapper,它可以在我们没有安装gradle的时候进行项目构建,下面我们会讲到.
> Windows和Linux上配置Gradle的开发环境方法差不多,这里就不一一介绍了.
