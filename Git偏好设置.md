# Git偏好设置

当我们把Git的环境配好，在Android Studio的偏好设置中只需要使用默认的配置就可以了。一般不需要特殊配置，但也不排除你有特殊的需求，那下面我们就介绍下Git的偏好设置。

### 设置步骤:

偏好设置: Version Control —&gt; Git

Path to Git executable:

Git执行路径,这里使用的是默认路径,如果你自定义了Git路径,这里要记得攺一下, 不然会报错的.

SSH executable:

执行SSH,默认是使用Android Studio内建的,你还可以选择使用Native\(本地\)的.

commit automatically on cherry-pick:

在cherry-pick时是否自动提交.

tips：cherry-pick可以选择某一个分支中的一个或几个commit来进行操作.

warn if crlf line separators are about to be committed:

如果回车换行符被提交是否警告

Warn when committing in detached HEAD or during rebase:

提交detached HEAD或rebase时是否警告.

tips： detached HEAD用来让HEAD随便指向某个commit id，rebase用来合并代码.

Update method:

选择代码更新方式:默认分支\/merge\/rebase

Auto-update if push of the current branch was rejected:

如果push当前分析被拒绝是否自动更新.

Allow force push:

是否允许强制push.







