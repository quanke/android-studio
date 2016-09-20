# Gradle Script

我们把项目查看模式切换成Android,所有的文件会通过类型进行归类,这个并不是实际在电脑中的文件结构哦，如果想看实际的物理结构请切换到Project.

切换成Android可以查看所有的Gradle Script:

每个文件后面都有一个灰色字体描述:

1.build.gradle: Project构建文件

2.build.gradle: Module构建文件

3.gradle.properties： gradle配置文件

4.proguard-rules.pro: 混淆规则配置文件

5.graddle-wrapper.properties: gradle wrapper属性文件

6.settings.gradle: 构建项目设置文件

7.local.properties: SDK、NDK配置文件

切换到Project模式我们来看看各个文件之间的关系:

项目中有一个app模块,这个模块是一个Android应用程序,它有自己的构建脚本和混淆配置文件.

项目根目录下的脚本文件是针对它所依赖模块的全局配置.

下面我们详细介绍一下每个文件的作用.

