基于一个 plugin 来理解 tapable 的使用

感觉插件实现的有问题 formatBytes 返回是个字符串，用的地方却期望是个对象

插件大概的意思是size check，根据size的大小，对比自己设置的阈值，提示报告

其核心还是让开发者在实现插件时，去理解tapable的作用，但没有具体讲tapable