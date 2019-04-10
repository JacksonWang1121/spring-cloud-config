Config Server分布式配置中心组件的创建过程
    1、添加依赖
        spring-cloud-config-server
        （加上spring-cloud-starter-netflix-eureka-server依赖后，会访问不到配置文件）
    2、在@SpringbootApplication的启动类上
        打上注解@EnableConfigServer
    3、配置application.properties
高可用的分布式配置中心（作为一个服务）的创建过程（以上过程为基础）：
    1、添加依赖
        spring-cloud-starter-netflix-eureka-client
    2、配置application.properties，指定服务注册中心地址
    3、在@SpringbootApplication的启动类上
        加上注解@EnableEurekaClient


http请求地址和资源文件映射如下:
    /{application}/{profile}[/{label}]
    /{application}-{profile}.yml
    /{label}/{application}-{profile}.yml
    /{application}-{profile}.properties
    /{label}/{application}-{profile}.properties

