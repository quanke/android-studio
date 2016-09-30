## 将Android Library打包成.aar

打开Gradle工具窗口,找到Android Library模块. 在 build任务中双击assemble.

任务执行成功以后,在mylibrary\/build\/outputs\/aar目录下就会打出.aar格式的包.

默认Debug和Release的AAR包都会打出来,当然你也可以选择只打Debug的包,双击assembleDebug任务就可以了. 只打Release的包同理.

