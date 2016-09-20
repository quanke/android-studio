# 项目全局配置文件:settings.gradle



默认的settings.gradle文件内容如下:

include ':app'

settings.gradle是项目的全局配置文件,主要声明一些需要加入构建的模块,本例中只有一个模块:app.

如果新增一个模块需要在这里添加配置,通过Android Studio添加依赖的module会自动在这里添加相应的配置的.

包含多个模块的格式是这样的:

include ':app',':other-module-name'

如果包含的是某个目录下的模块,格式是这样的:

include ':app', ':dir-name:other-module-name'

