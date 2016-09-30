# Mac OS 环境配置

## 配置JDK

第1步: 下载JDK

下载地址: JDK8: http:\/\/www.oracle.com\/technetwork\/java\/javase\/downloads\/jdk8-downloads-2133151.html

> Android Studio2.2以后要求必须使用JDK8。

选择Mac OS X x64下载:

![](/image/Chapter01/Mac OS 环境配置/JDK 8 下载.png)

第2步：安装JDK8

下载完成后，双击安装包，然后按照提示进行安装。

安装完成后的路径：

\/Library\/Java\/JavaVirtualMachines\/

如果你安装了多个JDK版本,这里会显示多个。

第3步：配置环境变量

先查看原来的java版本

```
java -version
```

再vim .bash\_profile 去配置JAVA\_HOME

```
JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_45.jdk/Contents/Home

PATH=$JAVA_HOME/bin:$PATH

CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar



export JAVA_HOME

export CLASSPATH

export PATH 
```
保存后去执行下面的命令，更新成功


```
source .bash_profile
```

```
java -version
```

## 配置Android Studio


## 配置Android的环境变量

