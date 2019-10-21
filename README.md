# Reptile
网络爬虫
对比新浪提供的API及传统的爬虫方式获取微博的优缺点，采用模拟登陆和网页解析技术，将获取的信息存入数据库中并进行分析。基于Python设计实现了新浪微博爬虫程序，可以根据指定的关键词爬取新浪微博用户的个人信息、微博评论、粉丝以及图片的获取。
为解决单机爬虫的瓶颈，我们进一步的展望是采用 python 开发的 Scrapy 框架，运用 Xpath 技术对下载的网页进行提取解析、运用 Redis 数据库做分布式、使用MongoDb 数据库做数据存储设计分布式爬虫。分布式爬虫采用的设计模式将会是C/S模式，依照主从结构设置一个Master服务器和多个Slave服务器，Master端管理Redis数据库和分发下载任务，Slave部署Scrapy爬虫提取网页和解析提取数据，最后将解析的数据存储在同一个MongoDb数据库中，从而将单机爬虫改进为分布式爬虫
