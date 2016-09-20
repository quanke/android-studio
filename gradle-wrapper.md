# Gradle Wrapper

## Gradle Wrapper是什么？

Gradle Wrapper可以理解为是对Gradle的一层封装,使用它可以在没有安装Gradle的系统上使用Gradle来构建项目.
## 如何做到的呢？

Gradle Wrapper通过两个脚本文件实现这一功能,一个是用于windows的批处理文件gradlew.bat,一个是用于Linux和Uninx的Shell脚本文件gradlew.使用Android Studio创建的项目默认为我们生成了Gradle Wrapper的文件结构.

在gradle/wrapper目录下有两个文件: gradle-wrapper.jar和gradle-wrapper.properties
gralde-wrapper.properties文件中声明了gradle的版本和下载地址.

```
#Mon Dec 28 10:00:20 PST 2015

distributionBase=GRADLE_USER_HOME

distributionPath=wrapper/dists

zipStoreBase=GRADLE_USER_HOME

zipStorePath=wrapper/dists

distributionUrl=https\://services.gradle.org/distributions/gradle-2.10-all.zip

```

在第一次使用gradlew进行项目构建的时候,Gradle Wrapper会自动下载gralde-wrapper.properties指定的gradle版本.
> 通过gradlew执行gradle构建跟直接使用gradle是一样的. 如果我们想直接使用gradle构建需要先配置环境变量.
