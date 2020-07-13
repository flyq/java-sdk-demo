# java-sdk-demo

## 安装 sdkman
参考：  
https://sdkman.io/install

最后效果：
```shell
$ sdk version
==== BROADCAST =================================================================
* 2020-07-10: Micronaut 1.3.7 released on SDKMAN! #micronautfw
* 2020-07-07: Jbang 0.33.0 released on SDKMAN! See https://github.com/jbangdev/jbang/releases/tag/v0.33.0 #jbang
* 2020-06-27: sbt 1.3.13 released on SDKMAN! #scala
================================================================================

SDKMAN 5.8.3+506
```

## 安装 gradle
参考：  
https://gradle.org/install/

最后效果：   
```shell
$ gradle  --version

------------------------------------------------------------
Gradle 6.5.1
------------------------------------------------------------

Build time:   2020-06-30 06:32:47 UTC
Revision:     66bc713f7169626a7f0134bf452abde51550ea0a

Kotlin:       1.3.72
Groovy:       2.5.11
Ant:          Apache Ant(TM) version 1.10.7 compiled on September 1 2019
JVM:          13.0.2 (Oracle Corporation 13.0.2+8)
OS:           Linux 5.3.0-62-generic amd64
```
## 新建一个 Java 项目(已新建好)
本项目参考这个文档新建了一个Java项目，因为已经建好，因此不需要再次新建：  
https://guides.gradle.org/building-java-libraries/


## 拉取代码
```shell
git clone https://github.com/flyq/java-sdk-demo.git
```

## 修改(已改好)
修改 src/main/java/demo/App.java 里面的逻辑:   
```java
CITAj citaService = CITAj.build(new HttpService("http://x.x.x.x:1337")); 		// http://x.x.x.x:1337 需要改为节点的RPC接口或者缓存服务器接口
```

修改 src/test/java/demo/AppTest.java 里面的测试逻辑；

修改 ./build.gradle 里面的Java依赖项：
```gradle
    compile 'com.citahub.cita:core:20.2.0'
```

## build
```shell
cd java-sdk-demo/

./gradlew build
```

## run
```shell
./gradlew run
```

然后就可以从区块链浏览器上查看对应的交易了。
