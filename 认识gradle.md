### Gradle是什么？

Gradle是一个自动化构建工具,采用Groovy的Domain Specific Language（领域特定语言）来描述和控制构建逻辑.它的特点是语法简洁、可读性强、配置灵活等等. 基于Intellij IDEA社区版本开发的Android Studio天生支持Gradle构建程序.

Gradle使用指南请看:https:\/\/docs.gradle.org\/current\/userguide\/userguide.html

Groovy是什么?

Groovy是一种基于JVM的敏捷开发语言,它结合了Python、Ruby、Smalltalk的许多强大特性. Groovy 代码既能够与 Java 代码很好的结合,也能够用于扩展现有的代码.

更多Groovy请参考:http:\/\/www.groovy-lang.org\/

Gradle的特点:

* Gradle支持多工程构建和局部构建.

* Gradle支持远程或本地依赖管理: 支持从远程maven仓库、nexus私服、ivy仓库以及本地仓库获取依赖.

* Gradle与Ant、Maven兼容.

* Gradle可轻松迁移: Gradle适用于任何结构的工程.我们可以在同一个开发平台平行构建原工程和Gradle工程.

* Gradle使用灵活: Gradle的整体设计是以作为一种语言为导向的,而非成为一个严格死板的框架.

* Gradle免费开源Gradle跟IDE集成的非常好

* Gradle可以更容易地集成到自动化构建系统


## Gradle中的Project、Task和Plugin

## 项目是什么？

项目\(project\)是指我们的构建产物（比如Jar包）或部署的产物（将应用程序部署到生产环境）,每个项目包含一个或多个任务.

## 任务是什么?

任务\(Task\)是指不可分的最小工作单元，代表一个逻辑上较为独立的执行过程,比如:编译、复制、打包.

## 插件是什么？

Gradle只是提供了构建项目的一个框架,所有有用的特性都由Gradle插件提供，一个Gradle插件能够：

* 向项目中添加新任务.
* 为新加入的任务提供默认配置，这个默认配置会在项目中注入新的约定\(如源文件位置\).
* 加入新的属性, 可以覆盖插件的默认配置属性.
* 为项目加入新的依赖.

更多请参考: [http:\/\/www.gradle.org\/docs\/current\/userguide\/standard\_plugins.html](http://www.gradle.org/docs/current/userguide/standard_plugins.html)

## 项目、任务和插件的关系是什么？

项目代表要被构建的组件或整个项目,它为任务提供了执行的上下文，而插件用来向项目中添加属性和任务.一个任务可以读取和设置项目的属性以完成特定的操作.

## 如何配置Gradle构建？

Gradle的构建肯定会包含下面这几个配置文件:

Gradle构建脚本（build.gradle）指定了一个项目和它的任务.

Gradle属性文件（gradle.properties）用来配置构建属性.

Gradle设置文件（gradle.settings）对于只有一个项目的构建而言是可选的,如果我们的构建中包含多于一个项目，那么它就是必须的.

因为它描述了哪一个项目参与构建.每一个多项目构建都必须在项目结构的根目录中加入一个设置文件gradle.settings.

