# Android应用程序配置

Name:

名字. 可以在工具栏运行应用程序配置的下拉列表中看到。

General:

在这里配置安装、启动、部署应用程序选项

Module:

列表中列出了当前项目中的所有模块,我们可以指定相应的模块来运行.

Installation Options: 安装选项

1.Deploy:下拉列表中列出了应用程序运行时的部署模式

有三个选项:

Default APK: 部署默认的APK, 运行时会先打包安装,再启动APK。

Custom Artifact: 部署自定义的APK, 会根据你选择的模块来选择对应的配置。

Nothing: 不做任何部署,运行时会直接启动应用,如果应用已经安装了会直接启动, 没有安装就会报错。

2.Install Flags: 给adb shell pm install 添加运行参数,参数参加在pm install后面。

Install Flags为空时,运行应用程序时执行的命令是这样的:

```
# 1.把打好的包放到手机中的/data/local/tmp/目录下

$ adb push /Volumes/MyApplication/app/build/outputs/apk/app-debug.apk /data/local/tmp/com.wirelessqa.myapplication

# 2.重新安装应用程序

$ adb shell pm install -r "/data/local/tmp/com.wirelessqa.myapplication"

pkg: /data/local/tmp/com.wirelessqa.myapplication

Success

```


如果添加一个参数-f

```
# 2.重新安装应用程序,在install后就多了个-f参数

$ adb shell pm install -f -r "/data/local/tmp/com.wirelessqa.myapplication"

pkg: /data/local/tmp/com.wirelessqa.myapplication

Success

```



