# 增加so文件

**JNI是什么?**

Android系统的底层库是由c\/c++编写，上层Android应用程序和应用程序框架通过JNI（JavaNative Interface\)调用底层接口.

Android使用JNI开发分两种情况：一是使用已经编译好的.so动态库；二是使用c\/c++源代码开发.

一些第三方的库出于性能或代码安全的目的,会将核心代码用C\/C++来实现,然后提供编译好的so文件或jar包给我们.

**so文件是什么?**

Android中用到的so文件是一个c++的函数库，apk或jar包中调用so文件时，需要将对应so文件打包进apk或jar包.

**如何加载so文件？**

假设你的so文件为:libBaiduMapSDK\_v350\_1.so

这样加载:

String libName = "BaiduMapSDK\_v350\_1"; \/\/ 注意:库名libName, 没有前缀lib和后缀.so

System.loadLibrary\( libName \); \/\/在使用前一定要先加载

**so文件应该放在哪里？**

在Eclipse中我们将so文件放到libs目录下就可以了, 那么在AndroidStudio中应该将so文件放到哪里呢？

放到moduleName\/src\/main\/jniLibs目录下，如果没有jinLibs目录就新建一个.

armeabi、armeabi-v7a、mips、x86这四个文件夹是干嘛的呢?

表示四种不同的cpu类型，不同的cpu的特性不一样,在使用so文件时注意区分.

可以直接复制so文件粘贴到对应的文件夹下

ok之后so文件就进来啦.

