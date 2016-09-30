# 创建app widget



App Widget是应用程序的窗口小部件,它可以被嵌入到其它应用程序中\(如桌面\)并接收周期性的更新.

创建Widget的一般步骤:

第1步:在res\/layout目录下创建一个Widget布局文件.

第2步:创建一个类继承AppWidgetProvider.

第3步:在res\/xml目录下创建一个XML文件,用来定义Widget的特性.

第4步:在AndroidManifest.xml中声明Widget.

使用Android Studio的模板功能,可以帮我们自动完成上面这些步骤.



### 操作步骤:



菜单栏: File —&gt; New —&gt; Widget —&gt; App Widget



然后弹出【New Android Component】界面:

