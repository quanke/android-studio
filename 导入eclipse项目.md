# 导入eclipse项目

原文地址：http:\/\/ask.android-studio.org\/?\/article\/21



本篇教程中使用  Eclipse ADT版本23.0.4。请尝试更新到该版本。

Android Studio默认使用 **Gradle** 构建项目， **Eclipse** 默认使用**Ant**构建项目。建议Android Studio导入项目时，使用 **Gradle** 构建项目。

## **导入 Eclipse 项目**

本例中，使用到的 **Eclipse** 项目结构如图：

![](/image/Chapter02/导入eclipse项目/Eclipse 项目结构.png)

**e-demo** 为主项目， **appcompat\_v7** 为 **library** 项目。

### **导入 Generate Gradle build files 项目**

**Google官方建议是通过本方法进行Android Studio导入 Eclipse 项目。**

这种方式有一个好处就是兼容 **Eclipse** 的文件目录结构，通过版本控制中的文件过滤，可以在一个项目组中，同时使用 **Eclipse** 和Android Studio。

**讲解1**

**File** --&gt; **Export**

![](/image/Chapter02/导入eclipse项目/Export.png)

**讲解2**

选择导出类型。选择 **Android** --&gt; **Generate Gradle build files** 。

![](/image/Chapter02/导入eclipse项目/Generate Gradle build files.png)

点击 **Next** 。

**讲解3**

很长一段英语（完全看不懂是什么意思）。

![](/image/Chapter02/导入eclipse项目/Import Instead.png)

点击 **Next** 。

**讲解4**

选择要导出的项目。

![](/image/Chapter02/导入eclipse项目/Export Generate Gradle Build files.png)

因为我的 **e-demo** 项目依赖了 **appcompat\_v7** 项目，所以我将 **e-demo** 和 **appcompat\_v7** 都选择了导出。

点击 **Next** 。

**讲解5**

最终确认要导出的项目。

![](/image/Chapter02/导入eclipse项目/Export Generate Gradle Build files Next.png)

**Force overriding of existing files** 表示覆盖导出文件。使用 **Generate Gradle build files** 的方式导出项目，会在项目目录中生成一些文件。这里的覆盖文件指的就是覆盖这些可能已经生成过的文件。如果你之前有使用这种方式导出过项目，建议勾选。

点击 **Finish** 。

![](/image/Chapter02/导入eclipse项目/Export Generate Gradle Build files Finish.png)

**讲解6**

这一步没有什么好说的，直接点击 **Finish** 。

**讲解7**

**Finish** 点击完毕，并没有弹出窗口显示导出的项目，就好像什么事情都没有做一样。其实，使用这个方式导出项目，是在项目中添加了一些文件，我们可以到项目目录下去看一看这些生成文件。

工作空间目录下

![](/image/Chapter02/导入eclipse项目/工作空间目录.png)



**e-demo** 目录下 

![](/image/Chapter02/导入eclipse项目/e-demo 目录下.png)



**appcompat\_v7** 目录下

![](/image/Chapter02/导入eclipse项目/appcompat_v7 目录.png)



我们可以发现：在工作空间目录下，多出了 **gradle** 文件夹和 **build.gradle** 、 **build.gradle** 、 **gradlew** 、**gradlew.bat** 、 **settings.gradle** 文件；在 **e-demo** 目录下多出了 **build.gradle** 文件； 在 **appcompat\_v7** 目录下多出了 **build.gradle** 文件。这些文件和文件夹都和 **Gradle** 有关系，用于构建项目。这些文件以及文件夹的作用，我们以后再说。



**讲解8**



由于 **Eclipse** 的 **ADT** 插件已经很久没有更新了，自动生成的 **Gradle** 编译设置已经跟不上Android Studio的更新速度，所以我们需要手动修改一些内容。



打开工作空间目录下的 **gradle** --&gt; **wrapper** --&gt; **gradle-wrapper.properties** 。修改一下内容：**distributionUrl=http\:\/\/services.gradle.org\/distributions\/gradle-a.b.c-all.zip** --&gt;**distributionUrl=https\:\/\/services.gradle.org\/distributions\/gradle-2.2.1-all.zip**



打开工作空间目录下的 **build.gradle** 文件。修改以下内容：



**classpath 'com.android.tools.build:gradle:0.x.+'** --&gt; **classpath 'com.android.tools.build:gradle:1.0.0'** 。



之所以这么设置，是因为： **Eclipse** 导出的 **Gradle** 设置已经不是Android Studio 1.0 所支持的 **Gradle** 已经 **Gradle**插件版本，需要手动更为支持的版本。否则轻则必须不能离线导入项目，重则项目导入失败。



**讲解9**



打开Android Studio，选择 **Open an existing Android Studio project**。 

![](/image/Chapter02/导入eclipse项目/Open an existing Android Studio project.png)

**讲解10**



此时会弹出一个框，让你选择文件夹，这个时候需要注意的就是，你需要选择原来的 **Eclipse** 的工作空间目录，而不是 **e-demo** 目录。 

![](/image/Chapter02/导入eclipse项目/Eclipse 项目结构.png)

点击 **OK** 。



**讲解11**



设置导入选项。 



![](/image/Chapter02/导入eclipse项目/设置导入选项.png)

此处有一些比较重要的设置需要讲解一下。



* **Gradle project** ：此处通常显示的路径并不是你的 **Eclipse** 的工作空间的目录，而是 **Eclipse** 的工作空间的目录中的 **gradle** 路径。你需要手动删除后面的 **gradle** ，否则项目导入，你是看不到你的代码的，只能看到**gradle** 目录下的内容。
* **Create directories for empty content roots automatically** ：不是很明白它的作用，一般默认即可。
* **Use default gradle wrapper\(recommended\)** 和 **Use local gradle disribution** ：这两个是让你设置使用的**Gradle** 。默认会勾选 **Use default gradle wrapper\(recommended\)** ，我们需要手动勾选 **Use local gradle disribution** 。
* **Gradle home** ：勾选 **Use local gradle disribution** 后此项编程可编辑状态，默认的此处的地址为Android Studio安装目录中的 **Gradle** 路径地址。此处可能会有一些错误的警告，提示内容为： **Gradle location is incorrect** 。而你的这个目录下，确实是有 **Gradle** 的。产生这个问题的原因，很可能是因为 **Gradle home** 选项中，路径中的斜杠为 **\/** 而不是 **\*\* 。你需要点击左右的文件选择按钮，重新选择到Android Studio安装目录中的 \*\*Gradle** ，问题即可解决。
* **Offline work** ：设置 **Gradle** 使用离线的方式导入项目。你可以勾选也可以不勾选。如果你有进行 **讲解8** 的操作，你则可以勾选，以离线的方式进行编译。



点击 **OK** 。之后便会看到编译进度条，根据每个人机器的配置，编译的时间不同。 

![](/image/Chapter02/导入eclipse项目/编译进度条.png)

编译完成之后，自动跳转到Android Studio的主页面。在编译的工程中，会有以下的弹框：

 

![](/image/Chapter02/导入eclipse项目/编译的工程中的弹框.png)

之所以有这个弹框，是因为Android Studio默认使用 **JAVA 1.7** 进行编译，如果你的项目不是 **1.7** ，则会弹框让你选择。建议选择 **Yes** ，因为当你使用 **JAVA 1.7** 的时候，只要不使用 **JAVA 1.7** 的资源自动释放这个新特性，能够完美得兼容 **JAVA 1.6** 的Android设备。



如果你看到下面这个界面，说明你已经导入成功了。 

![](/image/Chapter02/导入eclipse项目/导入成功.png)

### **直接导入 Eclipse 项目**

如果不使用 **Generate Gradle build files** 导出项目，可以使用Android Studio直接打开 **Eclipse** 工作空间，进行项目导入。





#### **不使用 Gradle 编译项目**

这种方式可以兼容`Eclipse`的文件目录结构，通过版本控制中的文件过滤，可以在一个项目组中，同时使用 **Eclipse** 和Android Studio。但是在Android Studio中并不是使用 **Gradle** 构建项目，而是使用的 **Ant** 。



**讲解12**



打开Android Studio，选择 **Import Non-Android Studio project**。 

