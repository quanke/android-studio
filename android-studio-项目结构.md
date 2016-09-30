# Android Studio 项目和模块



Android Studio中的两个重要的概念: 项目\(Project\)和模块\(Module\) .

模块\(Module\):

Module是一个可以单独的运行和调试的application或公共库,它相当于Eclipse当中的Project.



我们通常把一些公共的代码放到module当中,当你的APP需要添加一些依赖的库或者需要依赖一些公共的项目时可以导入module.

每个module中都有自己的build.gradle文件用来配置模块的构建任务.

在build.gradle文件中我们可以配置SDK版本、构建工具版本、应用程序版本、打包参数、模块的依赖等等.

项目\(Project\):

Project可以理解为一个完整的APP项目,它由application module和一些依赖的module组成, 相当于Eclipse当中的workspace.

一个Project中有多个module。

Project中也有一个build.gradle文件用来指定构建的项目和任务,当你导入或新建一个Module时,build.gradle会自动更新.

项目 VS 模块

Module相当于Eclipse当中的Project.Project相当于Eclipse当中的workspace.一个Project中可以包含多个Module.Module中的build.grade用于配置模块的构建任务.Project中的build.grade用于定构建的项目和任务.

