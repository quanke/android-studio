# 常用Gradle任务



1.查看gradle版本



```

$ ./gradlew -v

```



2.编译并打出Debug版本的包.



```

./gradlew assembleDebug

```



3.编译并打出Release版本的包.



```

./gradlew assembleRelease

```



4.执行检查并编译打包



```

./gradlew build

```



打出所有Release和Debug的包.



5.删除build目录



```

./gradlew clean

```



会把app下面的build目录删掉



6.编译打包并安装Debug版本的包



```

./gradlew installDebug

```



7.卸载Debug版本的包



```

./gradlew uninstallDebug

```



8.使用-info查看任务详情



```

./gradlew uninstallDebug -info

```

