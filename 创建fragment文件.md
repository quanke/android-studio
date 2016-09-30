# 创建Fragment文件

创建一个Fragment的一般步骤:

第1步: 在Layout目录下创建Fragment的布局文件.

第2步: 创建一个类文件,继承Fragment或者Fragment子类,并在onCreateView方法中加载布局文件.

第3步: 在Activity的布局文件中声明FragmentLayout.

使用模板基本上可以自动生成第1步和第2步.

如何使用Android Studio提供的模板快速创建Fragment及其所用到的布局文件呢？

### 操作步骤:

菜单栏: File —&gt; New —&gt; Fragment

Fragment\(Blank\):创建一个空白的Fragment

Fragment\(List\):创建一个空的Fragment,它包含一个网格列表.

Fragment\(with a + 1 button\):创建一个带有Google Plus +1按钮的Fragment

## 创建一个空白的Fragment

点击 【Fragment\(Blank\)】—&gt; 然后弹出【New Android Component】界面;

* FragmentName: 自定义的Fragment类名, 会继承Fragment. 本例中为BlankFragment.

* Create Layout XML?: 如果勾选,会同时创建BlankFragment类对应的布局文件,并在BlankFragment类中自动添加加载该布局文件的代码.

* Fragment Layout Name: BlankFragment类对应的布局文件名,会根据类名自动生成,可自定义.

* Include fragment factory methods?: 如果勾选,会在BlankFragment类中生成工厂方法.

* Include interface callback?: 如果勾选,会在BlankFragment类中生成回调接口.


## 

创建一个Fragment\(List\)

点击 【Fragment\(List\)】—&gt; 然后弹出【New Android Component】界面:

* Package name: 包名
* Object Kind: 对象类型
* Fragment class name: Fragment类的名字
* Column Count: 网格的列数
* Object content layout file name: 对象内容布局文件名
* List layout file name: 列表布局文件名
* Adapter class name: Adapter类名


