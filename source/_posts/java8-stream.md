---
title: java-java8-新特性02-StreamApi
date: 2019-03-15 20:18:59
tags: java
categories: java
---

### Stream API是对Java中集合操作的增强，可以利用它进行各种过滤、排序、分组、聚合等操作

```
\\ eg1：
list.stream().forEach(System.out::println);


\\ eg2:
List<String> userNames =
        users.stream()
        .filter(user -> user.getAge() > 20)
        .sorted(comparing(User::getCreationDate))
        .map(User::getUserName)
        .collect(toList());

```

###Stream接口中包含许多对流操作的方法

1. filter()：对流的元素过滤
2. map()：将流的元素映射成另一个类型
3. distinct()：去除流中重复的元素
4. sorted()：对流的元素排序
5. forEach()：对流中的每个元素执行某个操作
6. peek()：与forEach()方法效果类似，不同的是，该方法会返回一个新的流，而forEach()无返回
7. limit()：截取流中前面几个元素
8. skip()：跳过流中前面几个元素
9. toArray()：将流转换为数组
10. reduce()：对流中的元素归约操作，将每个元素合起来形成一个新的值
11. collect()：对流的汇总操作，比如输出成List集合
12. anyMatch()：匹配流中的元素，类似的操作还有allMatch()和noneMatch()方法
13. findFirst()：查找第一个元素，类似的还有findAny()方法
14. max()：求最大值
15. min()：求最小值
16. count()：求总数