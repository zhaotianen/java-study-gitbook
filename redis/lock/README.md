# redis分布式锁

## 1. 介绍

分布式锁的实现分为两部分，一个是单机环境，另一个是集群环境下的Redis锁实现。

### 1.1 什么是分布式锁

分布式锁是控制分布式系统或不同系统之间**共同访问共享资源的一种锁实现**，如果不同的系统或同一个系统的不同主机之间共享了某个资源时，往往需要互斥来防止彼此干扰来保证一致性

### 1.2 分布式系统需要具备哪些条件

1. 互斥性：在任意一个时刻，只有一个客户端持有锁
2. 无死锁：即使持有锁的客户端崩溃或者其他意外事件，锁仍然可以被获取
3. 容错：只要大部分 redis节点都活着，客户端就可以获取和释放锁

### 1.3 分布式锁的实现有哪些

1. 数据库
2. Memcached（add命令）
3. Redis（setnx命令）
4. Zookeeper（临时节点）
5. 等等



### 参考文章

[redis系列：分布式锁](<https://juejin.im/post/5b737b9b518825613d3894f4>)
