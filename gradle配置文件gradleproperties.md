# Gradle配置文件:gradle.properties

gradle.properties是gradle的配置文件，build.gradle通过读取这个文件配置的参数来进行相应的构建.

默认的gradle.properties文件内容如下:

```
# 设置整个项目的Gradle.

# IDE (e.g. Android Studio) users:

4# 通过IDE设置将会覆盖Gradle settings文件所有的设置.

# 关于如何配置构建环境的更多详情,请访问:

# http://www.gradle.org/docs/current/userguide/build_environment.html

# 指定用于守护进程的JVM参数.

# 该设置对调整内存设置特别有用.

# 默认值: -Xmx10248m -XX:MaxPermSize=256m

# org.gradle.jvmargs=-Xmx2048m -XX:MaxPermSize=512m -XX:+HeapDumpOnOutOfMemoryError -Dfile.encoding=UTF-8

# 配置完毕后, Gradle 将在并行模式下运行.(并行编译)

# 只应在解耦项目中使用此选项.更多详情, 请访问:

# http://www.gradle.org/docs/current/userguide/multi_project_builds.html#sec:decoupled_projects

# org.gradle.parallel=true

```

默认的gradle.properties文件内容为空,只有一些注释.可以在这里设置Gradle的代理在gradle.properties添加:

```
systemProp.http.proxyHost=Proxy Server

systemProp.http.proxyPort=Proxy port

# 设置代理的用户名和密码,如果没有就不用设置

systemProp.http.proxyUser=User

systemProp.http.proxyPassword=password

# 设置不需要代理的地址,多个地址使用或‘|’隔开

systemProp.http.nonProxyHosts=*.baidu.com|*.taobao.com

```