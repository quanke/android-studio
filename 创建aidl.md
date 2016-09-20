# 创建AIDL
[](http://quanke.name/2016/07/22/Android-Studio-Service-AIDL-%E8%AF%A6%E8%A7%A3/)
### **什么是AIDL？**

`AIDL`是 `Android Interface definition language`的缩写，它是一种`Android`内部进程通信接口的描述语言，通过它我们可以定义进程间的通信接口

### **AIDL可以解决什么问题？**

* 可以实现多个应用程序共享同一个Service的功能，比如：IM服务可以提供给多个APP使用，先在推送基本都是采取这种方案
* 可以跨进程调用服务里的方法

#### 实战演示：

##### **1.创建AIDL文件夹**

![](/image/Chapter02/创建AIDL/1.png)

##### **2.创建AIDL文件**

![](/image/Chapter02/创建AIDL/2.png)

##### **3.编写AIDL文件**

```
// IHandler.aidl
package name.quanke.aidldemo;

// Declare any non-default types here with import statements

interface IHandler {
    void connect();
}
```

##### **4.AIDL文件 生成接口**

![](/image/Chapter02/创建AIDL/4.png)

生成后的样子

![](/image/Chapter02/创建AIDL/3.png)

##### 

> 关于AIDL的使用，可以看我的博客，有详细讲解

[http://quanke.name/2016/07/22/Android-Studio-Service-AIDL-%E8%AF%A6%E8%A7%A3/](http://quanke.name/2016/07/22/Android-Studio-Service-AIDL-%E8%AF%A6%E8%A7%A3/)


