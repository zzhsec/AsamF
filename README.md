# AsamF
AsamF是一款集成多个网络资产测绘平台的搜索工具

AsamF，Asset survey and mapping V0.1.1

本程序仅供学习研究使用，禁止利用本程序对相关平台或其他企业或个人造成任何利益侵害！

将Fofa、Zoomeye、Quake、Hunter集成在一起。

本程序可以单独使用上述平台，也可以同时调用4个平台，因为4个平台的语法格式不同，因此调用4个平台聚合搜索的选项不支持关键字组合搜索，也不是所有的选项均支持4个平台。

1. 优化各个平台的取key，通过 -fk -hk -qk -zk 可以分别取key；

2. 新增了判断ip是否为蜜罐功能；

3. -domian、-app、-host、-title、-port、-server、-ih 这几个选项会聚合平台来搜索。具体见-h描述。

4. -fofatotal 可以配合 -fields 使用，默认值为title。

5. -zoomeyedomain 可以配合'-rs 1' 进行关联查询，默认不关联。

6. 修改了取数据方式。会根据查询数据结果数量来获取结果。使用Zoomeye、Quake、Hunter没有进行限制，因此存在结果数量太大，会一直获取到apikey的额度为0，使用时请注意。fofa不存在该问题。

7. 新增info功能，可以查询各个账户的信息。hunter不支持


<img width="1000" alt="image" src="https://user-images.githubusercontent.com/53268974/182889524-42832701-6557-4162-83cf-30f4e0415f04.png">

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182890438-246e67cc-ce0b-4d18-97d8-5fb9be7df87f.png">

<img width="400" alt="image" src="https://user-images.githubusercontent.com/53268974/182890536-e7b56ed3-8c2e-46ff-8e39-a920b2a7a406.png">

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182890860-5a7c58ef-742d-4406-9b28-3211b21dcd9f.png">


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182896433-c1e87adc-1927-40a5-be70-ee5da46e2da9.png">

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182896763-729d02ba-b8a5-4598-95b6-64c8d306e636.png">

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182897101-196c0cd4-5520-464e-b184-2c8438572471.png">

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182896763-729d02ba-b8a5-4598-95b6-64c8d306e636.png">

-fofahost 主机搜索

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976108-7cbbc2b7-01b9-426f-afbe-33511b3faf06.png">

-fofatotal 聚合功能

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976932-217db434-183a-4665-8134-75730837b109.png">


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976418-58d63eb4-dba3-4a06-b780-2e99b58a0593.png">


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976418-58d63eb4-dba3-4a06-b780-2e99b58a0593.png">

-zoomeyehost 

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976526-61842fc5-4bb7-47d0-b07a-3d7301183ad6.png">

-zoomeyeweb

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976646-1b951dc6-95af-4fd8-90c2-5a22aa943711.png">

-zoomeyedomain

<img width="808" alt="image" src="https://user-images.githubusercontent.com/53268974/182976855-bec3ee36-bc2d-40f4-a947-a2822060b754.png">










自行研究吧...

未来还会新增一些功能







