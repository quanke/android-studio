# Linux 环境配置



### 安装JDK

下载JDK8

下载地址:http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

先增加执行权限：sudo chmod 777 jdk-8u101-linux-x64.bin

新建一个文件夹：sudo mkdir /opt/java **"这个是要注意的，因为intel lij 对路径的识别只支持三个路径，所有，要把JDK安装在这三个之一：**`/usr/java`** or**` /opt/java`** or**`/usr/lib/jvm` 我就在这出了一个问题

移动到要安装的目录：sudo mv jdk-8u101-linux-x64.bin /opt/java

sudo /opt/java/jdk-8u101-linux-x64.bin

这个安装包的任务完成了，扫扫：sudo rm -f /opt/java/jdk-8u101-linux-x64.bin

### 配置JDK

```
sudo gedit ~/.bashrc 加上：

#set java environment

export JAVA\_HOME=\/opt\/java\/jdk1.8.0\_45

export JRE\_HOME=$JAVA\_HOME\/jre

export CLASSPATH=$CLASSPATH:$JAVA\_HOME\/lib:$JRE\_HOME\/lib

export PATH=$PATH:$JAVA\_HOME\/bin:$JRE\_HOME\/bin:$JAVA\_HOME\/lib:$JAVA\_HOME
```


`sudo gedit /etc/environment` 加上：

JAVA_HOME=/opt/java/jdk1.8.0_45 ”这个是我遇到第二个问题，不知道什么原因，最开始我是在/etc/profile配置额上边～/.bashrc加的那段，就是不行，找不到JAVA_HOME这个项，就直接放到这个文件了一份，ANDROID STUDIO就可以启动了。 之后又吧/etc\/profile的配置项挪到了～/.bashrc了， 我还很小白，现在还不知道是什么原因导致不能读到/etc/profile的配置项，猜测可能是没更新环境变量？有知道的帮忙回一下。

### 配置Android Studio

sudo mv android-studio-bundle-130.677228-linux.tgz /opt/ ”"我直接用的文档管理器解压再挪过去的

sudo tar zxvf android-studio-bundle-130.677228-linux.tgz

可以将目录改成你喜欢的名字：sudo mv /opt/and... /opt/android-studio

cd /opt/android-studio/bin

ls

sudo studio.sh

