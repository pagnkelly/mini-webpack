## 笔记

从入口文件看是实现了一个 Compiler 的实例，执行了run方法

### Compiler

complier创建实例时把plugin方法全都执行完了

run中是整体的主流程，执行了tapable的一些钩子，具体的底层处理还是在Compilation

最后把code生成导出

### Compilation

parse了代码

loader的执行是在这里的

建立图  建立依赖关系 

### parse

主要用了@babel/parser生成ast

@babel/traverse遍历ast节点 获取import节点，收集依赖

@babel/core改import为require

### ejs

可从ejs看出，前面针对代码的解析，处理为的还是把一个mapping给到require函数中，递归的方式执行了其中的方法
