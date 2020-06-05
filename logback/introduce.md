# 介绍
## 小试牛刀
### 要求
除了`logback-classic.jar`外，`logback-classic` 模块需要`slf4j-api.jar`和`logback-core.jar`在类路径中出现。
> 为了能跑这一章的演示代码，你必须保证引用了特定的依赖。 详情请见[启动页](http://logback.qos.ch/setup.html)

```java
package chapters.introduction

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

public class HelloWorld1{
    public static void main(String[] args){
      Logger logger = LoggerFactory.getLogger("chapters.introduction.HolloWorld1");
      logger.debug("Hello world")
    }
}
```
上面这几行代码先引用了`Logger`和`LoggerFactory`两个定义在SLF4J包
中的类。注意，这个例子中没有引用任何`logback`的类。在大多数的例子当中
你的类只需要引用`SLF4J`的类。

