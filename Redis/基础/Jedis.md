# Jedis

[Jedsi官网](https://redis.io/docs/connect/clients/java/#learn-more)

1. 引入依赖

![Alt text](image-28.png)

2. 建立连接

![Alt text](image-29.png)

3. 测试string

![Alt text](image-30.png)

4. 释放资源

![Alt text](image-31.png)

eg:
![Alt text](image-32.png)

# jedis连接池

jedis本身是线程不安全的,并且频繁的创建和销毁会有性能损耗.使用Jedis连接池来来提jedis直连方式

![Alt text](image-33.png)

![Alt text](image-34.png)

线程池的连接方式

![Alt text](image-35.png)