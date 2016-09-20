# 查看和执行Gradle任务

## 查看当前项目支持哪些Gradle任务

使用.\/gradlew task来查看当前项目支持哪些Gradle任务.

```
FirstApp$ ./gradlew task

:tasks



------------------------------------------------------------

All tasks runnable from root project(所有从项目根目录可运行的任务)

------------------------------------------------------------

Android tasks(Android 任务)

-------------

androidDependencies - 显示项目的Android依赖

signingReport - 显示每个变种版本的签名信息.

sourceSets - 打印出所有在这个项目中定义的source集合.

Build tasks(构建任务)

-----------

assemble - 编译并打出应用程序所有变种版本的包.

assembleAndroidTest -编译并打出所有测试应用的包.

assembleDebug - 编译并打出Debug版本的包.

assembleRelease - 编译并打出Release版本的包.

build - 执行所有检查并编译打包

buildDependents - 检查所有的依赖并编译打包.

buildNeeded - 检查所有的依赖并编译打包.

clean - 删除构建目录

compileDebugAndroidTestSources

compileDebugSources

compileDebugUnitTestSources

compileReleaseSources

compileReleaseUnitTestSources

mockableAndroidJar - 创建一个适用于单元测试的android.jar版本.

Build Setup tasks (构建设置任务)

-----------------

init - 被始化一个新的Gradle构建.

wrapper - 生成 Gradle wrapper文件

Help tasks(帮助任务)

----------

buildEnvironment - 显示项目根目录中声明的所有构建脚本的依赖

components - 显示项目根目录产生的组件

dependencies - 显示项目根目录中所有依赖的声明.

dependencyInsight - 显示并洞察项目根目录中一个特殊的依赖关系.

help - 显示帮助信息

model - 显示项目根目录的配置模型.

projects - 显示项目根目录中的子项目.

properties - 显示项目根目录的属性.

tasks - 显示从项目根目录可以运行的任务(

有些显示的任务可能属于子项目)

Install tasks(安装任务)

-------------

installDebug - 编译打包并安装Debug版本的包.

installDebugAndroidTest - 编译打包并安装Debug版本的测试包到设备上

uninstallAll - 卸载所有版本的包.

uninstallDebug - 卸载Debug版本的包.

uninstallDebugAndroidTest - 从设备上卸载Debug版本的Android测试包

uninstallRelease - 卸载Release版本的包.

Verification tasks(验证任务)

------------------

check - 运行所有检查.

connectedAndroidTest - 在已连接的设备上安装所有flavors(渠道包)并运行instrumentation测试

connectedCheck - 在当前已连接的设备上运行设备检测.

connectedDebugAndroidTest - 在已连接的设备上安装并运行Debug版本的测试.

deviceAndroidTest - 在所有提供的设备上安装并运行instrumentation测试.

deviceCheck - 在所有提供的设备和测试服务器上运行设备检测.

lint - 在所有变种版本上运行lint检测.

lintDebug - 在Debug版本上运行lint检测.

lintRelease - 在Release版本上运行lint检测.

test - 在所有变种版本上运行单元测试.

testDebugUnitTest - 在Debug版本上运行单元测试.

testReleaseUnitTest - 在Release版本上运行单元测试.

Other tasks (其它任务)

-----------

jarDebugClasses

jarReleaseClasses

transformResourcesWithMergeJavaResForDebugUnitTest

transformResourcesWithMergeJavaResForReleaseUnitTest

想查看所有任务和更多详情, 请运行gradlew tasks --all

想查看一个任务的更多详情, 请运行gradlew help --task <task>

BUILD SUCCESSFUL

Total time: 6.717 secs

这个构建可以更快, 请考虑使用Gradle守护: https://docs.gradle.org/2.10/userguide/gradle_daemon.html

```

## 执行Gradle任务

执行命令:

gradle + 任务名称

或

./gradlew + 任务名称

注意: Gradle的Android插件提供了四个顶级任务: 打包(assemble)、检测(check)、构建(build)、清理(clean),当我们执行一个顶级任务的时候会同时执行与其依赖的任务.

比如你执行: ./gradlew assemble

它会把你配置的所有构建类型(Build Types)全部打出来,默认的构建类型是Debug和Release,因此最起码它会执行两个任务:

gradlew assembleDebug

gradlew assembleRelease

如果有其它的构建类型,任务名应该是:

gradlew assemble+构建类型名

另外你还要知道,执行构建\(build\)任务会执行 检测\(check\)和打包\(assemble\)任务.

## 常用Gradle任务

1.查看gradle版本

$ ./gradlew -v

2.编译并打出Debug版本的包.

./gradlew assembleDebug

3.编译并打出Release版本的包.

./gradlew assembleRelease

4.执行检查并编译打包

./gradlew build

打出所有Release和Debug的包.

5.删除build目录

./gradlew clean

会把app下面的build目录删掉

6.编译打包并安装Debug版本的包

./gradlew installDebug

7.卸载Debug版本的包

./gradlew uninstallDebug

8.使用-info查看任务详情

./gradlew uninstallDebug -info

## Gradle工具窗口

Gradle工具窗口列出了当前项目和模块中支持的所有Gradle任务和运行配置，以方便我们快速操作.

### Tasks:

Tasks列表里的任务跟我们执行./gradlew task得到的任务列表是一样的.

把光标放在某个任务上面显示任务的描述信息:

双击任务即可执行.

任务执行结果:

点击Run工具栏左上角的切换按钮, 可以在任务执行模式和文本式之间切换.

Run Configurations:

Run Configurations列表中列出了项目中执行过的任务配置,这些配置都是执行任务时自动生成的.

想再次执行的时候可以在配置列表中直接选择.

可以在Run/Debug Configurations中对这些配置进行修攺.

