# 数据库
_不知道咋皮了，就这样吧_

## mysql
### linux连接mysql
``` linux
/opt/mysql/bin/mysql -ueasy7 -peasy7 EASY7
```
### show
查看当前连接数及信息
``` mysql
SHOW PROCESSLIST;
```
查看最大连接数
``` mysql
SHOW VARIABLES LIKE "%max_connections%";
```
修改最大连接数
/opt/mysql/etc/my.ini
### 常见sql优化

## oracle
### linux连接oracle

### oracle连接数
1. 查看当前连接数
``` oracle
select count(*) from v$session;
```
2. 查看数据库最大连接数
``` oracle
select value from v$parameter where name = 'processes';
```
3. 修改连接数
``` oracle
alter system set processes = 300 scope = spfile;
```
4. 关闭数据库
``` oracle
shutdown immediate;
```
5. 启动数据库
``` oracle
startup;
```