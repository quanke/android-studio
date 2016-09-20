# 解决Gradle下载太慢的问题

## 第一步: 首先我们要知道gradle从哪里下载,下载什么版本？

方法1：在gradle-wrapper.properties中查看gradle下载地址和版本

本例中,下载地址是：[https:\/\/services.gradle.org\/distributions\/gradle-2.10-all.zip](https://services.gradle.org/distributions/gradle-2.10-all.zip) ,版本是2.10.

方法2：去查看所有分发的gradle版本地址:[https:\/\/services.gradle.org\/distributions](https://services.gradle.org/distributions)

在这里可以查看到最新的gradle版本，点击可下载.

第二步: 下载完成后放到什么地方？

本例: \/Users\/quanke\/.gradle\/wrapper\/dists\/gradle-2.4-all\/3i2gobhdl0fm2tosnn15g540i0你的: \/Users\/你的用户名\/.gradle\/wrapper\/dists\/gradle-版本号-all\/一堆随机生成字符串，这一堆字符是随机生成的，每次发现新的可下载的版本的时候就会生成一堆新的字符,如果想让AndroidStudio识别我们的版本，需要先生成这堆字符哦。

可以先打开Android Studio看有没有生成这堆字符串,如果没有你就执行下命令喽.

第三步: 给gradle脚本设置可执行权限

本例: chmod +x \/Users\/quanke\/.gradle\/wrapper\/dists\/gradle-2.4-all\/3i2gobhdl0fm2tosnn15g540i0\/gradle-2.4\/bin\/gradle

你的: chmod +x \/Users\/你的用户名\/.gradle\/wrapper\/dists\/gradle-版本号-all\/一堆随机生成字符串\/bin\/gradle

然后重新打开Android Studio,gradlew命令就可以用啦.

下面我们不单纯的来讲Gradle,而是通过其在Android项目中的应用来一一讲解.

方法二: 设置代理

翻墙以后妈妈再也不用担心我的学习了.

