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

Class Name: 类名,继承AppWidgetProvider.\[图片\]Placement: Widget 放在哪儿.

1.Home-screen and Keyguard: 在主屏幕和锁键上.

2.Home-screen only: 仅在主屏幕上.

3.Keyboard only\(API 17+\): 仅在锁键上\(只支持Android4.2及以上版本\).

Resizable\(API 12+ \): Widget是否可调整大小,只支持Android 3.1及以上版本.

1.Horizontally and vertically: 水平和垂直显示时可调整.

2.Only Horizontally: 仅水平时可调整.

3.Only vertically: 仅垂直时可调整.

4.Not resizable: 不可调整.

* Minimum Width: 最小宽度,参照左边预览窗口的单元格.

* Minimum Height: 最小高度,参照左边预览窗口的单元格.

* Configuration Screen:勾选后会生成widgets配置activity.


使用默认配置,点击【Finish】后创建成功.

