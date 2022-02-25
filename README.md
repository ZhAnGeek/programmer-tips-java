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

### 如何通过groovy编写表达式
```java=
        List<String> childrenExpression;
        switch (conditionNodeType) {
            case LEAF:
                return data.generateExpression();
            case OR:
                childrenExpression = getChildren().stream().map(conditionNodeDTO -> "(" + conditionNodeDTO.travelConditionTree() + ")").collect(Collectors.toList());
                return Joiner.on(" || ").join(childrenExpression);
            case AND:
                childrenExpression = getChildren().stream().map(conditionNodeDTO -> "(" + conditionNodeDTO.travelConditionTree() + ")").collect(Collectors.toList());
                return Joiner.on(" && ").join(childrenExpression);
            default:
                return "";
        }

```
