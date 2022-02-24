# programmer-tips-java

### 如何让一个组件初始化时执行

```java=
@PostConstruct
```


```java=
implement interface InitializingBean
implement method afterPropertiesSet() throws Exception;
```

### 如何配置dataSource
dataSource可以获取到Connection并且管理
