# AsamF

AsamF是一款集成多个网络资产测绘平台的一站式企业信息资产收集工具。

请勿利用本程序损害任何个人或企业的利益，造成一切影响，开发者将不承担任何责任！

 [下载链接](https://github.com/Kento-Sec/AsamF/releases)
 
 ***
 
## v0.1.7 更新

1. 修正了fofa、quake、zoomeye的一些问题
2. fofa增加了total子命令，可以输出全部数据（因为fofa官方的限制，每次访问最大只有2000，因此为了不影响效率，把该功能单独出来了）
3. 增加了fofa、zoomeye、hunter、shodan、quake的语句规则查询。（此处制表代码复制fofax，利用这个表格，补充了其他平台的查询语法。感谢fofax。）
4. 增加了查询最近漏洞的功能。使用方法：AsamF vuln
5. quake增加了查询的起始页选项：-start 以及获取多少页的选项：-size。quake的接口改为深度查询接口。数据量越大等待时间会长些，数据会一次过展示出来。另外他们部分data里的部分字段的数据提取是有问题。有了解的可以研究下。另外不建议购买quake的会员，不值，他们的逻辑用zoomeye可以代替。
6. zoomeye可以使用-page来获取多少页。一页是20条数据。

***

## 0x00 简介

AsamF集成了Fofa、Hunter、Quake、Zoomeye、Shodan、爱企查、Chinaz、0.zone、subfinder。AsamF支持Fofa、Hunter、Quake、Zoomeye、Shodan、Chinaz、0.zone配置多个Key，在搜索前加入对应选择key的flag可以自由切换需要使用的key。可以通过info命令来查看该key的账户信息。Union命令将联合Fofa、Hunter、Quake、Zoomeye内置的语法格式进行搜索。所有的命令、子命令都支持短命令使用。

<img width="1728" alt="-h" src="https://user-images.githubusercontent.com/53268974/190156066-4e59dcae-cd8a-414d-a44d-c5ab07d136fe.png">

***

## 0x01 配置

AsamF会在~/.config/asamf/目录下生成config.json文件。如果你有多个key，按照json的格式录入即可，建议键值按照阿拉伯数字依次录入,方便以阿拉伯数字来切换key。

自动结果保存在~/asamf/目录下。

***

## 0x02 爱企查

爱企查支持cn、cnf子命令。

cn:**重点功能** 一站式企业信息、资产收集。使用方法: AsamF a cn -q 公司名

**公司名 ---> URL ---> 主机查询 ---> 备案、控股、分支机构 ---> 子域名 ---> 信息系统、泄露邮箱、人员信息、App资产、目录、代码收集。**

cnf: 批量对公司名获取url、ip地址。使用方法: Asamf a cnf -q target.txt

--percentage, -p :根据控股比例进行递归。默认不递归,即为0。使用方法: AsamF a -q 公司名 -p 100

<img width="1000" alt="a-h" src="https://user-images.githubusercontent.com/53268974/190160160-c2ed04d2-1997-4303-8f8f-69cf22d7da71.png">

 

***

## 0x03 Fofa

fofa支持info、iu、il、host、total以及file子命令。


info:查询账户信息。 使用方法：AsamF f info -fk 1

iu:根据icon url进行搜索。使用方法：AsamF f iu -q xxx

il:根据本地icon文件进行搜索。使用方法：AsamF f il -q xxx

host:进行主机搜索。使用方法：AsamF f h -q xxx

total:进行聚合搜索。使用方法：AsamF f t -q xxx

file:批量搜索。使用方法：AsamF f f -q xxx

若不使用子命令，直接使用-q选择进行搜索。

<img width="1000" alt="fofa-h" src="https://user-images.githubusercontent.com/53268974/190156396-c35402d4-7d21-421d-b275-f1abca322bff.png">

***

## 0x04 Zommeye

Zoomeye支持info、web、domain、host子命令。

info:查询账户信息。使用方法：AsamF z info -zk 1

web:web应用搜索。使用方法：AsamF z w -q xxx

domian:子域名搜索。使用方法：AsamF z d -q xxx

host:主机搜索。使用方法：AsamF z h -q xxx

若不使用子命令，直接使用-q选择进行搜索。

<img width="1000" alt="zoomeye-h" src="https://user-images.githubusercontent.com/53268974/190158265-fdb4c3d4-6d55-48fb-80b1-d063e69e99f7.png">

***

## 0x05 Hunter

info: 子命令查询会扣除10个积分。(因为他们不提供这个接口)

Asamf h -q xxx

<img width="1000" alt="h-h" src="https://user-images.githubusercontent.com/53268974/190161655-ea71583c-1977-4bb3-8dc0-ec3994a5f20b.png">

***

## 0x06 Quake

Quake支持info、hy子命令。

hy: 查询目标是否为蜜罐。使用方法: AsamF q hy -q ip

Quake查询功能将根据你的账户类型来查询数据量。注册会员:500; 高级会员:5000; 终身会员:10000。

<img width="1000" alt="截屏2022-09-14 21 07 25" src="https://user-images.githubusercontent.com/53268974/190162257-2de325c4-451b-4712-a2c8-8193383ee412.png">

***

## 0x07 Shodan

Shoan支持: p(port)、hi(host information)、dd(dns domain)、ds(dns resolve)、dr(dns reverse)、qt(query tags)、info、apiinfo命令。

-facets选项支持：domain. asn、domain、city、device、ip、isp、org、os、vuln、tag、version(详情见shodan语法）。

<img width="1000" alt="截屏2022-09-14 21 08 43" src="https://user-images.githubusercontent.com/53268974/190163240-1ca3dc99-fbf6-485b-8297-7a82020e4ef9.png">


***

## 0x08 Union

Union是fofa、zoomeye、hunter、quake使用联合查询的命令。内置了domain、app、server、port、host、title、body语法结构。直接输入要查询的内容即可，不需要写查询语法。

domain: 使用方法: AsamF u d -q baidu.com

app: 使用方法: AsamF u a -q apache

port: 使用方法: AsamF u p -q 8080


<img width="1000" alt="截屏2022-09-14 21 15 12" src="https://user-images.githubusercontent.com/53268974/190164060-d4b2f0f2-1631-4cbd-b29d-e133f95434c5.png">

***

## 0x09 0.zone

0.zone支持: system、email、app、directory、person、code子命令。

system: 查询信息系统。使用方法: AsamF 0 s -q 公司名

email: 查询信息系统。使用方法: AsamF 0 e -q 公司名

app: 查询信息系统。使用方法: AsamF 0 a -q 公司名

directory: 查询信息系统。使用方法: AsamF 0 d -q 公司名

person: 查询信息系统。使用方法: AsamF 0 p -q 公司名

code子命令: 查询信息系统。使用方法: AsamF 0 c -q 公司名

如果不使用子命令直接使用-q flag。将会执行全部功能。

使用方法: AsamF 0 -q 公司名


<img width="1728" alt="截屏2022-09-14 21 33 20" src="https://user-images.githubusercontent.com/53268974/190168130-f1a36eb2-bf0f-43f9-9dfd-67713514b8a6.png">



***

## 0x10 Chinaz

Chinaz支持ip、icp、weight、whois、whoisreverse

使用方法: 

AsamF c ip -q ip

AsamF c icp -q xxx

AsamF c wt -q xxx

AsamF c ws -q xxx

AsamF c wr -q xxx





***

## 0x11 sd

sd是子域名收集。

使用方法: AsamF sd -q baidu.com

其他功能会调用到sd。

***

## 0x12 myip

myip查询你的互联网ip: 使用方法: AsamF myip











