# 模块构建配置文件:build.gradle

Module:build.gradle是用来配置模块的构建任务.

默认的build.gradle文件内容如下:

```
//插件:

//这个module是一个android程序,使用com.android.application

//如果是android库,应该使用com.android.library

apply plugin: 'com.android.application'

android {//android程序构建需要配置的参数

//编译使用的SDK版本

compileSdkVersion 23

//buildtool版本

buildToolsVersion "23.0.2"

defaultConfig {//默认配置

applicationId "com.wirelessqa.basebuildsample" //apk包名

//最小SDK版本

minSdkVersion 16

//目标SDK版本

targetSdkVersion 23

//version code

versionCode 1

//应用程序的版本

versionName "1.0"

//android单元测试test runner

testInstrumentationRunner "android.support.test.runner.AndroidJUnitRunner"

}

//构建类型, 此处配置debug和release版本的一些参数,像混淆、签名配置.

buildTypes {

//release版本的配置

release {

//是否开启混淆

minifyEnabled false

//指定混淆文件及混淆规则配置文件的位置

proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'

 }

 }

}

//模块依赖

dependencies {

//编译依赖libs目录下所有jar包

compile fileTree(dir: 'libs', include: ['*.jar'])

//编译依赖appcompat库

compile 'com.android.support:appcompat-v7:23.4.0'

}

```

模块构建配置文件:build.gradle也可以在项目结构中配置,下面我们详细介绍一下.

