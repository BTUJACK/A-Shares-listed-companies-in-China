# 爬取中国大陆A股上市公司名单，并保存到数据库MySQL中


用数据库MySQL存储结果

#爬虫流程：
#1
模拟浏览器向服务器发出请求，然后处理响应，最常用的函数就是requests下面的get请求

#2
BeautifulSoup解析网页
利用pandas库中的read_html方法快速抓取网页中常见的表格型数据。
prettify()优化代码,[0]从pd.read_html返回的list中提取出DataFrame
rename将中文名改为英文名，便于存储到mysql及后期进行数据分析

#3
打开数据库
但是这种安装使用的命令是 /usr/local/mysql/bin/mysql -u root -p来开启mysql
// 进入mysql（要求输入mysql登录密码）
mysql -u root -p
// 退出mysql
exit

sudo mysql.server start
sudo mysql.server stop
sudo mysql.server restart

建立数据库
在数据库建立存放数据的表格

#4
写入数据库

如果想把数据存储到数据库mysql中，就要借助pymysql来操作

#5
main函数循环页数



参考
#下载数据库MySQL，然后要建立一个数据库：在控制栏输入：mysql> CREATE DATABASE WADE;

#mac安装MySQL的方法可以参考文章https://blog.csdn.net/BTUJACK/article/details/83749094

#MySQL可视化软件参考https://blog.csdn.net/BTUJACK/article/details/83750137

// 进入mysql（要求输入mysql登录密码）
mysql -u root -p
// 退出mysql

遗留问题：MySQL数据库可视化软件SequelPro无法打开，导致无法可视化
