# Gradlew配置文件:gradle-wrapper.properties

gradle-wrapper.properties 是gradle wrapper的配置文件.

默认的gradle-wrapper.properties文件内容如下:

```
#Mon Dec 28 10:00:20 PST 2015

distributionBase=GRADLE_USER_HOME

distributionPath=wrapper/dists

zipStoreBase=GRADLE_USER_HOME

zipStorePath=wrapper/dists

distributionUrl=https\://services.gradle.org/distributions/gradle-2.10-all.zip

```

一般这个文件是不用动的,除非你想手动指定gradle的版本,可以修攺distributionUrl.
也可以在Project Structure —> Project中设置Gradle version.

