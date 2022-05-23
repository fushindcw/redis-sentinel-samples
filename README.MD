# docker redis哨兵模式搭建  

## 一、基础配置  
|节点|IP|端口|备注|
|----|----|----|----|
| sentinel1 | 127.0.0.1 | 26379 | 哨兵1 |  
| sentinel2 | 127.0.0.1 | 26380 | 哨兵2 | 
| sentinel3 | 127.0.0.1 | 26381 | 哨兵3 | 
| redis-master | 127.0.0.1 | 6379 | 默认主redis | 
| redis-slave1 | 127.0.0.1 | 6380 | 默认从redis1 | 
| redis-slave2 | 127.0.0.1 | 6381 | 默认从redis2 |   

## 二、注意  
在使用docker进行部署时，如果采用默认配置，会导致哨兵提供容器内部ip，导致应用无法访问。  
所以在进行redis配置的时候，需要加上以下一个配置  
> replica-announce-ip "192.168.0.35"  

## 三、参考资料  
- [Redis哨兵模式(一主两从三哨兵)](https://blog.csdn.net/qq_36120342/article/details/118897643)  
- [关于redis哨兵判断监视节点是否宕机的原理，redis哨兵Sdown，Odown](https://blog.csdn.net/weixin_30329623/article/details/95551492)  
- [Redis的 slave-announce-ip sentinel announce-ip 介绍](https://www.jianshu.com/p/b9e2f39f191f)
- [docker redis的哨兵模式搭建——遇坑笔记](https://blog.csdn.net/a1076067274/article/details/109263303)