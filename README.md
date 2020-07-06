# java-sdk-demo

## 拉取代码
```shell
git clone git@github.com:flyq/java-sdk-demo.git
```

## 修改
修改App.java 里面的:   
```java
CITAj citaService = CITAj.build(new HttpService("http://x.x.x.x:1337")); 		// http://x.x.x.x:1337 需要改为节点的RPC接口或者缓存服务器接口
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
