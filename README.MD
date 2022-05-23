# docker redis哨兵模式搭建  

## 基础配置  
|节点|IP|端口|备注|
|----|----|----|----|
| sentinel1 | 127.0.0.1 | 26379 | 哨兵1 |  
| sentinel2 | 127.0.0.1 | 26380 | 哨兵2 | 
| sentinel3 | 127.0.0.1 | 26381 | 哨兵3 | 
| redis-master | 127.0.0.1 | 6379 | 默认主redis | 
| redis-slave1 | 127.0.0.1 | 6380 | 默认从redis1 | 
| redis-slave2 | 127.0.0.1 | 6381 | 默认从redis2 | 