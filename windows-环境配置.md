# Windows 环境配置

## 配置JDK

**下载JDK8**

下载地址：http:\/\/www.oracle.com\/technetwork\/java\/javase\/downloads\/jdk8-downloads-2133151.html

![](/image/Chapter01/Windows 环境配置/下载 JDK8.png)

选择自己合适的平台，下载

**安装JDK**

下载完成后双击安装,并按照提示一步一步直到完成安装。

> 建议默认安装

安装时请记住JDK的安装位置,后面我们配置环境变量的时候要用到。

**配置环境变量**

右击计算机 —&gt; 属性 —&gt; 高级系统设置 —&gt; 环境变量

新建系统变量JAVA\_HOME —&gt; 变量值为刚才安装的JDK的路径

在系统变量`path`中添加 `%JAVA_HOME%\bin`

新建系统变量`CLASS_PATH` —&gt; 添加变量值`%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;`

注意：如果 `CLASS_PATH`或者 `path`中有其他配置，请在后面增加 `;` 再增加我们需要的内容，尤其是CLASS\_PATH 需要注意

到此为止环境变量配置完毕,下面来验证下是否配置成功.

终端输入`javac`,如果显示帮助信息就证明配置正确了.

```


C:\Users\yurong>javac

用法: javac <options> <source files>

其中, 可能的选项包括:

 -g 生成所有调试信息

 -g:none 不生成任何调试信息

 -g:{lines,vars,source} 只生成某些调试信息

 -nowarn 不生成任何警告

 -verbose 输出有关编译器正在执行的操作的消息

 -deprecation 输出使用已过时的 API 的源位置

 -classpath <路径> 指定查找用户类文件和注释处理程序的位置

 -cp <路径> 指定查找用户类文件和注释处理程序的位置

 -sourcepath <路径> 指定查找输入源文件的位置

 -bootclasspath <路径> 覆盖引导类文件的位置

 -extdirs <目录> 覆盖所安装扩展的位置

 -endorseddirs <目录> 覆盖签名的标准路径的位置

 -proc:{none,only} 控制是否执行注释处理和/或编译。

 -processor <class1>[,<class2>,<class3>...] 要运行的注释处理程序的名称; 绕过默

认的搜索进程

 -processorpath <路径> 指定查找注释处理程序的位置

 -parameters 生成元数据以用于方法参数的反射

 -d <目录> 指定放置生成的类文件的位置

 -s <目录> 指定放置生成的源文件的位置

 -h <目录> 指定放置生成的本机标头文件的位置

 -implicit:{none,class} 指定是否为隐式引用文件生成类文件

 -encoding <编码> 指定源文件使用的字符编码

 -source <发行版> 提供与指定发行版的源兼容性

 -target <发行版> 生成特定 VM 版本的类文件

 -profile <配置文件> 请确保使用的 API 在指定的配置文件中可用

 -version 版本信息

 -help 输出标准选项的提要

 -A关键字[=值] 传递给注释处理程序的选项

 -X 输出非标准选项的提要

 -J<标记> 直接将 <标记> 传递给运行时系统

 -Werror 出现警告时终止编译

 @<文件名> 从文件读取选项和文件名

```

## 配置Android Studio

**下载Android Studio**

你可以到这里http:\/\/developer.android.com\/sdk\/index.html下载可执行文件进行安装.

也可以到这里下载最近的beta版本http:\/\/tools.android.com\/recent试用,beta版本不用安装,可以多个版本一起使用。



## 启动Android Studio



下载完成后 —&gt; 解压 —&gt; 进入到android\/bin目录 —&gt; 双击studio64\(如果操作系统是32位 双击 studio\)启动Android Studio.



## 配置Android的环境变量

