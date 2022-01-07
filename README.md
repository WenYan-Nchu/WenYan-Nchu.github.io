# 实时计算课程大作业 实时数据可视化界面
* ## 1.课题背景
> 某在线电子图书商城当前注册会员数有近千万会员，遍布于全国多个省份，日常在线业务量较大。为了提高商城的用户知名度，该公司拟计划开展大型促销活动（类似于双十一的电商购物活动）。为了准确、实时统计当前销售数量，公司拟委托你开发一个促销活动的大数据看板，用于当日活动启动后销售订单实时数据的变化情况。

> 老师给出了一个生成数据的软件，它会自己将数据写入到本地的mysql当中，然后就要就利用数据编写一个实时数据看板。
* ## 2.项目说明
> 本项目主要是使用canal读取MySQL的binlog文件，将读取到的信息发送到kafka集群中，然后通过flink处理后写入redis数据库中，最后用flask读取数据，ajax接收并更新界面的数据以达到实时看板的功能。

> 编程语言：
>> scala 2.11.5
>> jdk 1.8.0_281
>> python 3.8（推荐anaconda）
> 组件版本：
>> canal.deployer-1.1.5
>> kafka_2.11-0.10.0.1
>> flink-1.10.1-bin-scala_2.11
>> redis
> 可视化组件版本
>> flask 1.1.2
