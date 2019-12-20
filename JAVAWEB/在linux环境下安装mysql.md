### 在linux环境下安装mysql

##### 1.下载安装vm虚拟机

官网下载vm进行傻瓜式安装即可：可以指定安装目录，便于查找

 虚拟机安装包（这里提供的是12版本的）链接：https://pan.baidu.com/s/1bqh606z 密码：fabh 

##### 2.下载安装Centos7

在华为镜像网站找到Centos7dvd 进行下载

![image-20191211112137749](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191211112137749.png)

![image-20191211112202619](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191211112202619.png)

![image-20191211112226181](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191211112226181.png)

 下载完成后进行安装 https://blog.csdn.net/hsxy123123/article/details/103063121 



##### 3.华为镜像网站下载mysql

找到linux版本

![image-20191211112725822](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191211112725822.png)



##### 4.利用xshell连接虚拟机将MySQL传入虚拟机

查看ip地址命令：ipconfig

没有的的话就用：ip adress

![image-20191211113242712](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191211113242712.png)

在xshell 进行连接

![image-20191211113342988](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191211113342988.png)

点击确定 输入linux账号密码即可

xshell远程传输文件

https://blog.csdn.net/weixin_37909391/article/details/80530575

##### 5.安装mysql

过程如下

linux 删除组：

步骤 1：#vi /ect/group,查看用户组信息,用户组GID,查看完成 Esc->:->q 退出
2：#vi /ect/passwd 查看用户,以及用户对应组,找到GID为 用户组的用户,查看完成 Esc->:->q 退出
3：#userdel 用户
4：#groupdel 用户组完成

 https://blog.csdn.net/drf91519/article/details/78515258  （mysql 5.5版本）

https://blog.csdn.net/qq_40181063/article/details/90713153（mysql8.0.16版本）：注意配置文件问题不要直接复制



tar命令

　　解包：tar zxvf FileName.tar

　　打包：tar czvf FileName.tar DirName

 

gz命令

　　解压1：gunzip FileName.gz

　　解压2：gzip -d FileName.gz

　　压缩：gzip FileName

　　.tar.gz 和 .tgz

　　解压：tar zxvf FileName.tar.gz

　　压缩：tar zcvf FileName.tar.gz DirName

  压缩多个文件：tar zcvf FileName.tar.gz DirName1 DirName2 DirName3 ...

 

bz2命令

　　解压1：bzip2 -d FileName.bz2

　　解压2：bunzip2 FileName.bz2

　　压缩： bzip2 -z FileName

　　.tar.bz2

　　解压：tar jxvf FileName.tar.bz2

　　压缩：tar jcvf FileName.tar.bz2 DirName

 

bz命令

　　解压1：bzip2 -d FileName.bz

　　解压2：bunzip2 FileName.bz

　　压缩：未知

　　.tar.bz

　　解压：tar jxvf FileName.tar.bz

 

Z命令

　　解压：uncompress FileName.Z

　　压缩：compress FileName

　　.tar.Z

　　解压：tar Zxvf FileName.tar.Z

　　压缩：tar Zcvf FileName.tar.Z DirName

 

zip命令

　　解压：unzip FileName.zip

　　压缩：zip FileName.zip DirName