# ConstraintLayout约束

**1.ConstraintLayout基本界面**

更新Android Studio 2.2之后，更新了布局设计器，同时，引人了ConstraintLayout，这一布局，旨在降低布局层级，其主要界面如下所示：

![](/image/Chapter03/ConstraintLayout约束/ConstraintLayout主界面.png)

这个界面主要分成下面几个部分：

* 左侧边栏，包括Palette组件库和Component Tree

* 中间是布局设计器，包括两部分，左边是视图预览，右边是布局约束

* 右侧边栏，上面是类似盒子模型的边界和大小布局设计器，下面是属性列表


在熟悉了界面之后，我们要做的就是理解，什么是ConstraintLayout。ConstraintLayout的核心，实际上就是『约束』，这个翻译很直接，也很准确，它可以说是一个强化的 RelativeLayout，只不过比RelativeLayout增加了更多的约束条件和方式，从这一点上去理解，就很容易接受了。

> 在第一次引人ConstraintLayout的时候，Android Studio会自动去下载依赖，等他自动完成安装即可。 最后，在build.gradle中会添加一行依赖：
> 
> ```
> compile 'com.android.support.constraint:constraint-layout:1.0.0-alpha8'
> ```

Google提供了一个CodeLab来帮助开发者熟悉这个布局，地址如下所示：

https:\/\/codelabs.developers.google.com\/codelabs\/constraint-layout\/index.html\#0

同时，2016IO上Google也给出了一个Topic来讲解，地址如下所示：

https:\/\/youtu.be\/sO9aX87hq9c

**2.ConstraintLayout约束类型**

简单的说，约束，就是组件与组件之间的关系，借用官网上的一张图，我们来解释下：

![](/image/Chapter03/ConstraintLayout约束/两个Button直接的关系.png)

这里展示的，就是左右两个Button直接的关系，这实际上就是一个简单的相对布局方式，下面我们来看一下具体的约束类型。

当我们点击一个控件的时候，它的显示效果如图所示：

![](/image/Chapter03/ConstraintLayout约束/点击一个控件的时候，它的显示效果.png)

这里主要包含几种类型的约束

* 尺寸约束

* 边界约束

* 基准线约束


我们一一来看。

### **尺寸约束**

尺寸约束使用的是『实心方块』，如图：

![](/image/Chapter03/ConstraintLayout约束/实心方块.png)

这个很好理解，就是调整组件的大小。

### **边界约束**

边界约束使用的是『空心圆圈』，如图：

![](/image/Chapter03/ConstraintLayout约束/空心圆圈.png)

边界约束，是使用最多的约束，它用于建立组件与组件之间、组件与Parent边界之间的约束关系，实际上，就是确定彼此的相对位置。

### **基准线约束**

基准线约束，使用的是『空心圆角矩形』，如图：

![](/image/Chapter03/ConstraintLayout约束/空心圆角矩形.png)

基准线约束，是让两个带有文本属性的组件进行对齐的，可以让两个组件的文本按照基准线进行对齐。唯一要注意的是，你需要把鼠标放在控件上，等基准线约束的图形亮了，才可以进行拖动。

### **清除约束**

通过工具栏上的『清除约束』按钮，或者是控件上的悬浮提示，都可以清除一个控件的所有约束条件，如图：

![](/image/Chapter03/ConstraintLayout约束/清除约束按钮.png)

掌握好这几种约束条件的使用后，就可以自己去尝试下了，我们只要拖一个控件，来体验下。

**3.约束示例**

这里我把官网上的几个Demo的动图Copy过来：

## ![](/image/Chapter03/ConstraintLayout约束/Demo动图1.gif)

![](/image/Chapter03/ConstraintLayout约束/Demo动图2.gif)

![](/image/Chapter03/ConstraintLayout约束/Demo动图3.gif)

![](/image/Chapter03/ConstraintLayout约束/Demo动图4.gif)

![](/image/Chapter03/ConstraintLayout约束/Demo动图5.gif)

**4.自动约束Autoconnect**

在布局设计器的菜单栏上，有一个『磁铁』一样的图标，如图：

![](/image/Chapter03/ConstraintLayout约束/自动创建组件间的约束关系按钮.png)

默认这个按钮就是打开的，通过这个，我们可以实现组件约束的自动创建，Demo示例如图：

![](/image/Chapter03/ConstraintLayout约束/Demo动图6.gif)

这个和PPT里面拖动布局的时候，会弹出对齐的基准线，然后帮你自动居中这些功能类似。实际测试下来，这个功能可以很方便的在拖动组件的时候，帮你写好约束，但有些精确的调整，还是需要手动去创建的。

**5.约束推断Inference**

在布局设计器的菜单上，还有一个『灯泡』一样的按钮，通过这个按钮，可以帮我们自动创建组件间的约束关系，他分析的是一个组件附近的组件，并根据当前在设计面板中的位置来创建约束关系，如图所示：

![](/image/Chapter03/ConstraintLayout约束/自动创建组件间的约束关系按钮.png)

约束推断这个功能非常强大，我们只需要把组件拖到一个地方，然后就可以通过推断，来完成最基本的约束创建，最后，手动进行完善即可。

## ![](/image/Chapter03/ConstraintLayout约束/自动创建组件间的约束关系demo.gif)

## 

**6.View Inspector**

## Inspector界面就是设计布局的右边栏，包含了一个类似盒子模型的布局检查器和对应属性的属性列表，如图所示：

![](/image/Chapter03/ConstraintLayout约束/Inspector界面.png)

属性这一块我们就不看了，和大家在XML中写的属性是一样的，只不过这里通过可视化的方式弄出来了，这个之前就有了，我们主要来看下上面的那个界面。

![](/image/Chapter03/ConstraintLayout约束/properties_1.png)

这上面的ID，不多说了，这个盒子四周的线，代表着我们的Margin设置，在工具栏上，还可以设置Margin的基数，对于MD设计风格，这个基数一般是8dp，所以，这里可以选择X8的Margin：

![](/image/Chapter03/ConstraintLayout约束/properties_margin.png)

另外，最外面边框上还有两个带数字的小圆圈，这个就是控制相对位置的比例的，如图：

![](/image/Chapter03/ConstraintLayout约束/控制相对位置的比例demo.gif)

通过这个比例的设置，我们天然就自带了百分比布局。

最后，最难理解的就是盒子里面的那四根线，如图：

![](/image/Chapter03/ConstraintLayout约束/盒子里面的那四根线.png)

这里的四根线，在点击后，会发生变化，总共有以下几种：

### **Fixed**

![](/image/Chapter03/ConstraintLayout约束/Fixed.png)

这样一个类型的线，可以让你写定具体的大小数值。

### **Wrap Content**

![](/image/Chapter03/ConstraintLayout约束/Wrap Content.png)

这个就是Wrap Content的含义，包裹内容，没有发生变化。

### **AnySize**

![](/image/Chapter03/ConstraintLayout约束/AnySize.png)

这个就是最难理解的，它表示组件会占用所有的可用空间来适应约束，类似线性布局中，设置width=0，weight=1的方式。

## 

**7.Align**

![](/image/Chapter03/ConstraintLayout约束/Align.png)

在工具栏中，可以使用对齐工具，快速给选定组件设置对齐约束，如图：

我们可以来演示下：

## ![](/image/Chapter03/ConstraintLayout约束/Align_demo.gif)

**8.Pack**

在工具栏中，可以使用Pack工具，快速对组件进行编组操作，如图：

## ![](http://mmbiz.qpic.cn/mmbiz_gif/5micibPI4OJJCNYS3wAycUjHnptF5AOjopTxU5aLgMInpAyqDtBRFDq9OTxSygpWhFnWBZhLDBnUa8ggyoYCnkrw/0?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

## 

**9.快捷布局**

## 在一个组件上点击右键，可以快速创建一些布局的快捷设计，如图所示：

在这里，可以快速设置组件的居中，对齐等方式。

## ![](/image/Chapter03/ConstraintLayout约束/创建布局的快捷设计.png)

**10.GuideLine**

为了更加灵活的布局，ConstraintLayout还提供了一个GuideLine，如图所示：

![](/image/Chapter03/ConstraintLayout约束/GuideLine.png)

你可以为布局添加水平和竖直引导线，针对这条线来作为基准线布局，如图所示：

## ![](/image/Chapter03/ConstraintLayout约束/添加水平和竖直引导线.png)

## 

**11.ConstraintLayout布局转换**

通过Android Studio，我们可以很方便的把一个普通布局转化为ConstraintLayout，在布局设计器的左边栏下面的Component Tree来进行转换，如图所示：

![](/image/Chapter03/ConstraintLayout约束/ConstraintLayout布局转换.png)

转换还是很赞的，但目前还没试过复杂的布局是否有问题。

**12.从代码角度理解ConstraintLayout属性**

ConstraintLayout被称为增强的RelativeLayout，是有它的原因的，相对布局提供了layout\_toBottomOf类似这样的属性来控制组件间的相对位置，那么ConstraintLayout实际上也是一样的，我们来看这样一个属性：

```
app:layout_constraintTop_toBottomOf
```

他代表的是『期望组件的顶部，与指定组件的底部对齐』，那么了解了这个解释方式，其它的属性就很好理解了，所以说，虽然ConstraintLayout不太建议通过代码来布局了，但能理解代码的含义，对理解ConstraintLayout布局是非常有帮助的。

