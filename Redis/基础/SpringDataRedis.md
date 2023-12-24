# SpringDataRedis

springData是spring中数据操作的模块,包含对各种数据库的集成,其中对Redis的集成模块就叫做springDataRedis

[官网](https://spring.io/projects/spring-data-redis/)

![Alt text](image-36.png)

springDataRedis中提供了RedisTemplate工具类,其中封装了各种对Redis的操作.并且将不同数据类型的操作API封装了不同的类型中:

![Alt text](image-37.png)

# 操作

1. 引入依赖

![Alt text](image-38.png)

2. 配置文件

![Alt text](image-39.png)

![Alt text](image-42.png)

3. 注入RedisTemplate

![Alt text](image-40.png)

4. 编写测试

![Alt text](image-41.png)