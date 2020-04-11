# eureka-server
spring-cloud
服务注册与发现  Eureka

本学习项目分别对应  
1.单节点server
2.高可用2个server
3.高可用3个server
以及相关注意细节

说明：
  高可用启动：
  打成jar包,分别启动
  java -jar xxxx.jar --spring.profiles.active.eureka1
  java -jar xxxx.jar --spring.profiles.active.eureka2  
  java -jar xxxx.jar --spring.profiles.active.eureka3
  
  
  
实验：
  启动2~3台server，可以相互注册。停掉一台模拟宕机，其他继续工作，实现高可用。
  一般并不是server越多越好，太多了反而影响性能，占用太多资源。
  
客户端使用eureka-client，注册服务要注册到多个server。
正常不宕机，只注册一台，其他也会同步，但是不是真正意义的高可用。
  