# Remote.Quartz.Jobs

很多应用系统中我们常常要定时执行一些任务，与服务器巡检
*例如：数据库死锁检测，硬盘检测，业务数据定时回传，定时作业，缓存数据的定时更新、定时发送邮件，订单系统判断

*当维护的机器过多，需要耗费较大人力，每次操作较为重复，因此需要在服务器上安装服务进行定时作业，并且可以允许快速自动更新服务。

*安装作业的机器可能对外不开放端口但是可以访问互联网如（客户服务器机器）

*当调度作业一多某个时间段返回的数据过多，消费端添加RabbitMQ队列支持，webapi采用nginx负载 数据库采用mongo

 
# 后续待完善功能

*分布式高可用：后续可以通过同一个作业在多台机器上通过锁机制保证只有一台执行（进行中）

*可视化报表ELK展示

*aspnet core 支持支持linux

*后端管理服务代码

*集成微服务surging改造（大家多关注）
https://github.com/dotnetcore/surging

 
# 如何使用

因为最近才空出时间来进行维护之前的项目，程序已应用于内部几十家服务器上部署并运行，代码较乱未梳理凑活着看，还未上传完成（如后端API）
coder们改造重点看MZ.jobs项目，然后根据WebAPI接口编写后台支持。webhost下 JobsController
有需要问题请提issue。

 
分布式远程调度器

1.通过远程API动态调整对应执行机器上的调度服务，支持远程个性化参数支持

2.可支持远程更新服务，只需定时上传作业业务类到更新站点下（）

3.使用aspNet webAPI， Quartz ，ELK日志展示， MongoDB(作业日志存储）rabbitMQ nginx

[Alt text](https://github.com/zluckymn/Remote.Quartz.Jobs/jobs.png)

ps对Only.jobs增加远程自动化更新与优化调度操作
https://github.com/mamingbo/Only.Jobs
 
