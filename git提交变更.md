# Git提交变更

当本地文件变更以后,可以通过VCS —&gt; Git —&gt; Commit File 弹出提交变更窗口.

当然,分支合并过后也会弹出提交变更窗口.

### 配置提交信息

提交变更窗口中你可以选择Change list,也可以选择要提交的变更文件,默认是全选的.

在Author中选择或者输入作者名字.选择Amend commit\(修订提交\)会在Commit Message中添加上一次的提交信息.

在提交之前,你还可以选择做一些代码优化的工作,比如: Reformat code\(格式化代码\)、Rearrage code\(重新排列代码\)、Optimize imports\(优化导入\)、Perform code analysis\(执行代码分析\)、Check TODO\(检查待办事项\)、Cleanup\(清理\)、Update copyright\(更新版权声明\).

点击某个变更的文件, 在Details中会显示本地和远程的对比.

### 提交变更

当配置好提交信息以后,将鼠标放到Commit上面,会弹出提交操作列表.

Commit and Push: 将本地变更的文件提交到本地仓库,然后推到远程仓库.Create Patch: 将本地变更的文件作为补丁创建.Commit: 将本地变更的文件提交到本地仓库.

这里我选择Commit and Push：

如果你选择了提交之前进行一些代码检查或优化,会先执行优化.

如果点击Review可以查看代码分析出来的问题,查看以后觉得没问题,重复上面的操作\(Android Studio会有记录\)

如果点击Commit会直接提交.

Commit成功后会提示Push到远程仓库.

默认提交到当前分支，你也可以选择其它分支.

点击Push将本地变更推送到选择的远程分支.

