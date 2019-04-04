Config Server分布式配置中心组件的创建过程
    1、添加依赖
        spring-cloud-config-server
    2、在@SpringbootApplication的启动类上
        打上注解@EnableConfigServer
    3、配置application.properties



http请求地址和资源文件映射如下:
    /{application}/{profile}[/{label}]
    /{application}-{profile}.yml
    /{label}/{application}-{profile}.yml
    /{application}-{profile}.properties
    /{label}/{application}-{profile}.properties

