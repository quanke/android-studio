# Android应用程序配置

**Name:**

名字. 可以在工具栏运行应用程序配置的下拉列表中看到。

**General:**

在这里配置安装、启动、部署应用程序选项

**Module:**

列表中列出了当前项目中的所有模块,我们可以指定相应的模块来运行.

### Installation Options: 安装选项

**1.Deploy:下拉列表中列出了应用程序运行时的部署模式**

有三个选项:

**Default APK**: 部署默认的APK, 运行时会先打包安装,再启动APK。

**Custom Artifact:** 部署自定义的APK, 会根据你选择的模块来选择对应的配置。

**Nothing:** 不做任何部署,运行时会直接启动应用,如果应用已经安装了会直接启动, 没有安装就会报错。

**2.Install Flags: 给adb shell pm install 添加运行参数,参数参加在pm install后面。**

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

### Launch Option: 启动选项

**1.Launch提供了四个选项.**

Default Activity: 启动默认Activity,运行时会启动默认的MainActivity,如果没有会报错。

Specified Activity: 指定启动的Activity

在输入框中输入Activity的名字,输入时会有智能联想:

如果记不住名字,还可以搜索:

或在项目结构中查找:

定义好启动Activity后,运行应用时这个Activity就会被启动。


Nothing: 运行时不会启动任何Activity.

URL: 在这里可以指定启动的scheme.

**2.Launch Flags: 给adb shell am 添加运行参数,参数添加在命令的最后面.**

Deployment Target Options: 部署目标选项

**Target:**


**Show Device Chooser Dialog**：选择此选项,每次运行时都会弹出选择设备对话框。

**USB Device:** 使用USB连接的设备

**Emulator: **使用模拟器.

Use same selection for future launches:

如果勾选此项,以后运行时都使用同样的选择,不需要再次选择了.

**Miscellaneous:**

在这里配置日志和安装选项

**Logcat:**

Show logcat automatically: 运行时自动显示logcat日志。

Clear log before launch: 启动前清空日志。
Installation Options:

Skip installation if APK has not changed： 如果代码没有变更,运行时跳过安装。

Force stop running application before launching activity。

启动Activity前强制关闭运行的应用程序.

Debugger:

在这里配置调试类型.

Debug类型包括: Java、Native、Hybrid.Profiling:在这里配置图形跟踪选项.

disable precompiled shaders and programs: 禁用预编译着色器和程序.

Before launch:

在这里可以配置运行之前需要执行的任务,默认会执行Make.

添加任务

点击+添加一个新的任务:

![](/image/Chapter12/Android 应用程序配置/新的任务.png)

