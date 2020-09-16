**Spring Cloud**为开发者提供工具，帮助开发者快速构建一些在分布式系统上的通用模式。
比如，设置管理，服务发现，智能路由，微代理，控制总线，一次性令牌，全局锁等。
##特征
· 分布式、版本式设置  
· 服务注册和发现  
· 路由  
· S2S调用  
· 负载平衡  
· Circuit Breakers  
· leadership election和集群状态  
· 分布式消息  

**Spring Cloud**带来申明式的方法，并且你经常仅仅改变classpath和注解就会获得大量的特征
比如下面这个发现的客户端。  
```java
@SpringBootApplication
@EnableDiscoveryClient
public class Application {
	public static void main(String[] args) {
		SpringApplication.run(Application.class, args);
	}
}
```

##主要的项目
#### Spring Cloud Config
中心化全部配置管理，由**git**仓库支持。资源配置直接映射（map）至Spring环境
但是这些配置可以被非spring应用使用。  