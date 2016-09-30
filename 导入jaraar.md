# 导入Jar\/AAR

`.aar`格式的包是Android独有的第三方库\(Android Library\), 包含了可重用的java文件和Android组件.我们可以通过新建module创建自己的Android Library,然后打包成.aar格式的包与别人共享,使用方法跟jar包基本一样.

### 导入步骤：

菜单栏: File —&gt; New —&gt; New Module… —&gt; Import .JAR\/.AAR Package



选择aar包存放路径,并给子项目命名.



完成后可以看到作为模块导入的.aar文件.



mylibrary-debug的构建文件build.gradle:


```
configurations.create\("default"\)

artifacts.add\("default", file\('mylibrary-debug.aar'\)\)
```

Project的settings.gradle文件中自动添加了mylibrary-debug模块:

```
include ':app', ':phonetabletmodule', ':mylibrary', ':mylibrary-debug'
```


