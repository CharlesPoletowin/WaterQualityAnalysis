This project is for INESA Water Analysis,   

2020年7月16日接手前人留下的数据分析代码。  

当前库主要为处理210的jupyter无法访问内网数mongoDB据库而设立。

因此采用在210上运行代码生成json文件，在本地将json文件写入相关collection.

2020-7-23 修正由于部分siteno对应数据的日期不是完整的（只到19年6月）导致的错误。

2020-07-24 经过查询确认当前前端连接的数据都在210.*.*.108而不是210.*.*.81服务器上，也不在91的服务器上

2020-07-24 修复分析过程产生的假json的bug，目前当成json的list处理

1. waterDataToMongodb.py文件是处理数据的主要文件

2. WaterQualityDetection3.py是 class，不直接运行，通过waterDataToMongodb调用
