# SQL
SQL
任务一是软件安装和配置，以及一些数据库理论知识储备。
学习内容是指需要在博客文章中总结的知识点，包括但不仅限于这些知识点。比如一些安装过程中的报错及解决办法也可以写。

1.软件安装及服务器设置。
   教程 http://www.runoob.com/mysql/mysql-install.htm

创建my.ini配置文件，下载的免安装版客户端。

[mysql]
设置mysql客户端默认字符集
default-character-set=utf8
[mysqld]
设置3306端口
port = 3306
设置mysql的安装目录
basedir=D:\\web\\mysql-8.0.15-winx64
设置 mysql数据库的数据的存放目录，MySQL 8+ 不需要以下配置，系统自己生成即可，否则有可能报错
datadir=C:\\web\\sqldata
允许最大连接数
max_connections=20
服务端使用的字符集默认为8比特编码的latin1字符集
character-set-server=utf8
创建新表时将使用的默认存储引擎
default-storage-engine=INNODB


安装始终报错。D:\web\mysql-8.0.15-winx64\bin>mysqld install
'mysqld' is not recognized as an internal or external command,
operable program or batch file.
   
最后用官方的直接安装包搞定


3.数据库基础知识
数据库定义：数据库（Database）是按照数据结构来组织、存储和管理数据的仓库。
数据库是一些关联表的集合。
每个数据库都有一个或多个不同的 API 用于创建，访问，管理，搜索和复制所保存的数据。

关系型数据库：是建立在关系模型基础上的数据库，借助于集合代数等数学概念和方法来处理数据库中的数据。
RDBMS 即关系数据库管理系统(Relational Database Management System)的特点：
1.数据以表格的形式出现
2.每行为各种记录名称
3.每列为记录名称所对应的数据域
4.许多的行和列组成一张表单
5.若干的表单组成database

数据表: 表是数据的矩阵。在一个数据库中的表看起来像一个简单的电子表格。
列: 一列(数据元素) 包含了相同的数据, 例如邮政编码的数据。
行：一行（=元组，或记录）是一组相关的数据，例如一条用户订阅的数据。
行列构成二维表
主键：主键是唯一的。一个数据表中只能包含一个主键。你可以使用主键来查询数据。
外键：外键用于关联两个表。


4.MySQL数据库管理系统
数据表：你往文件柜里放资料时，并不是随便将它们扔进某个抽屉就完事了，而
是在文件柜中创建文件，然后将相关的资料放入特定的文件中。
在数据库领域中，这种文件称为表。表是一种结构化的文件，可用来存 储某种特定类型的数据。表可以保存顾客清单、产品目录，或者其他信 息清单。
视图：通俗的讲，视图就是一条SELECT语句执行后返回的结果集。所以我们在创建视图的时候，主要的工作就落在创建这条SQL查询语句上。
存储过程：存储过程是为了完成特定功能的SQL语句集，经编译创建并保存在数据库中，用户可通过指定存储过程的名字并给定参数(需要时)来调用执行。

