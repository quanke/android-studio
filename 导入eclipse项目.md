# 导入eclipse项目

本篇教程中使用  Eclipse ADT版本23.0.4。请尝试更新到该版本。

Android Studio默认使用 **Gradle** 构建项目， **Eclipse** 默认使用**Ant**构建项目。建议Android Studio导入项目时，使用 **Gradle** 构建项目。



## **导入 Eclipse 项目**

本例中，使用到的 **Eclipse** 项目结构如图： 



**e-demo** 为主项目， **appcompat\_v7** 为 **library** 项目。





### **导入 Generate Gradle build files 项目**

**Google官方建议是通过本方法进行Android Studio导入 Eclipse 项目。**



这种方式有一个好处就是兼容 **Eclipse** 的文件目录结构，通过版本控制中的文件过滤，可以在一个项目组中，同时使用 **Eclipse** 和Android Studio。



**讲解1**



**File** --&gt; **Export** 





点击 **Next** 。



**讲解3**



很长一段英语（完全看不懂是什么意思）。 



点击 **Next** 。



**讲解4**



选择要导出的项目。 



因为我的 **e-demo** 项目依赖了 **appcompat\_v7** 项目，所以我将 **e-demo** 和 **appcompat\_v7** 都选择了导出。



点击 **Next** 。



**讲解5**



最终确认要导出的项目。 





**Force overriding of existing files** 表示覆盖导出文件。使用 **Generate Gradle build files** 的方式导出项目，会在项目目录中生成一些文件。这里的覆盖文件指的就是覆盖这些可能已经生成过的文件。如果你之前有使用这种方式导出过项目，建议勾选。



点击 **Finish** 。



**讲解6**



这一步没有什么好说的，直接点击 **Finish** 。 



**讲解7**



**Finish** 点击完毕，并没有弹出窗口显示导出的项目，就好像什么事情都没有做一样。其实，使用这个方式导出项目，是在项目中添加了一些文件，我们可以到项目目录下去看一看这些生成文件。



工作空间目录下 







