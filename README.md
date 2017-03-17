# Mysql 修改密码

第一步：

           关闭mysql,使用命令：

           sudo /usr/local/mysql/support-files/mysql.server stop
          或者在系统偏好设置里最下面，找到mysql，stop mysql server
第二步：
 
          进入目录
 
           cd /usr/local/mysql/bin 
 
第步：
        获取权限
 
        sudo su 
 
第四步：
 
        重启服务
        ./mysqld_safe --skip-grant-tables &
 
第五步:
        重新开个终端（command+n）
第六步：
       执行脚本：
      alias mysql=/usr/local/mysql/bin/mysql
第七步：
      输入mysql，进入mysql模式；
第八步：
      use mysql,进入mysql数据库
第九步：
       获取权限
       flush privileges;
第十步：
      修改密码：
       set password for 'root'@'localhost'=password('root');
第十一步：
        验证：
     mysql -u root -p       输入密码即可
到此结束！！！
mac 下启动停止mysql:
启动mysql：
 
sudo /usr/local/MySQL/support-files/mysql.server start
停止mysql: 
sudo /usr/local/mysql/support-files/mysql.server stop
重启mysql：
 
sudo /usr/local/mysql/support-files/mysql.server restart
