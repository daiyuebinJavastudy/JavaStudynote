# MYSQL学习笔记续

### 一 约束

 

含义：为了限制表中的数据，以保证表中数据的准确性和可靠性，也可以说一致性； 

**1.六大约束：** 

1.非空：NOT  NULL     用于保证该字段的值不能为空 

2.默认：DEFAULT       保证该字段有默认值 

3.主键：PRIMARY KEY         用于保证该字段的值具有唯一性并且非空，比如学号 员工编号，只要是主键默认非空 

4.唯一：UNIQUE    用于保证字段值唯一，可以为空 比如座位号 

5.检查约束：CHECK(MySQL中不适用)   比如年龄，性别 

6.外键：FOREIGN KEY  用于限制两张的关系，保证该字段的值必须来自主键关联列的值 

在从表添加外键约束，用于引用主表主键的值 ，比如学生的专业编号，员工表的工种编号 



**2.添加约束的时机：** 

​	1.创建表时 

​	2.修改表时 

**3.约束添加的分类：** 

​	1.列级约束 

​	六大约束都支持，但检查约束在mysql中没有效果 

​	2.表级约束 

​	除了非空和默认，其余都可

**4.添加列级约束语法**

注意：列级约束只支持 默认，非空，主键，唯一

语法：

```mysql
#添加列及约束

create table stuinfo(
				id INT PRIMARY KEY,#主键
				stuName VARCHAR(20) NOT NULL,#非空
				seat INT UNIQUE,#唯一
				gender	CHAR(1) CHECK(gender='男'OR gender='女'),
				age INT DEFAULT 18,#默认
				majorid INT  REFERENCES major(id) #添加外键，这样添加不支持；
)
create table major(
				majorId INT PRIMARY KEY,
				majorNmae VARCHAR(20) NOT NULL
				
);
#查看索引
show INDEX from stuinfo
#删表
drop table if exist  表名;
```

**5.添加标级约束语法：**

语法：在各个字段最下面

【CONSTRAINT 约束名】  约束类型（字段名） *注：约束名可以不写，*

```mysql
#添加表级约束
create table stuinfo(
				id INT ,
				stuName VARCHAR(20) NOT NULL,
				seat INT ,
				gender	CHAR(1),
				age INT DEFAULT 18,#默认
				majorid INT,
				CONSTRAINT PK PRIMARY KEY  (id),
				CONSTRAINT UQ UNIQUE(seat),
				CONSTRAINT CK CHECK(gender='男'or gender='女'),
				CONSTRAINT FK_major_stuinfo FOREIGN KEY (id) REFERENCES major(majorId)
		);
```



什么时候添加表级约束，什么时候添加列级约束？

通用写法;

```mysql
CREATE TABLE stuinfo(
							id INT PRIMARY KEY,
							stuName VARCHAR(20) NOT NULL,
							seat INT UNIQUE,
							gender	CHAR(1) CHECK(gender='男' or gender='女'),
							age INT DEFAULT 18,#默认
							majorid INT,
							CONSTRAINT FK_major_stuinfo FOREIGN KEY (majorid) REFERENCES major(majorId)
);
```



**面试：关于主键和唯一的区别**？

主键（PRIMARY KEY）：保证唯一性，不能为空，一张表只能有一个主键，允许组合主键

唯一(UNIQUE):保证唯一性，能为空，一张表可有多个，允许组合主键



什么叫做组合主键：两个字段组成一个主键(一般不推荐使用);

```mysql
create table stuinfo(
				id INT ,
				stuName VARCHAR(20) NOT NULL,
				seat INT ,
				gender	CHAR(1),
				age INT DEFAULT 18,#默认
				majorid INT,
				CONSTRAINT PK PRIMARY KEY  (id,stuName),
				CONSTRAINT UQ UNIQUE(seat),
				CONSTRAINT CK CHECK(gender='男'or gender='女'),
				CONSTRAINT FK_major_stuinfo FOREIGN KEY (majorid) REFERENCES major(majorId)
		);
```

外键（FOREIGN）:

1.要求在从表设置外键关系

2.从表的外键字段的值类型必须和主表的关联的值类型一致或者兼容，名称无要求

3.主表的关联的列类型必须是一个key：（类型：主键或者唯一） 

4.插入数据：先插入主表，再插入从表，  删除数据时：先删除从表，再删除主表；



##### 6.修改表时添加约束

```mysql
#添加非空约束
ALTER TABLE stuinfo1 MODIFY COLUMN stuName varchar(20) not null;
#添加默认约束
ALTER TABLE stuinfo1 MODIFY COLUMN age int default 18;
#添加主键 1.列级 2.表级
ALTER TABLE stuinfo1 MODIFY COLUMN id int PRIMARY KEY;
ALTER TABLE stuinfo1 ADD PRIMARY KEY(id);

#添加唯一  1.列级 2.表级
ALTER TABLE stuinfo1 MODIFY COLUMN seat INT UNIQUE;
ALTER TABLE stuinfo1 ADD UNIQUE(seat);

#添加外键
ALTER TABLE stuinfo1 ADD FOREIGN KEY(majorId) REFERENCES major(majorid);

```

##### 7.修改表时删除约束

```mysql
#删除非空约束
ALTER TABLE stuinfo1 MODIFY COLUMN stuName varchar(20)null;
#删除默认约束
ALTER TABLE stuinfo1 MODIFY COLUMN age int;
#删除主键 
ALTER TABLE stuinfo1 DROP PRIMARY KEY;

#删除唯一  
ALTER TABLE stuinfo1 DROP INDEX seat;


#删除外键
ALTER TABLE stuinfo DROP FOREIGN KEY FK_major_stuinfo;
```

##### 8.表的复制

```MYSQL
#只复制表的结构
CREATE TABLE TAL_NAME LIKE 复制的表名;
#复制表的内容
CREATE TABLE TAL_NAME 
SELECT * FROM 复制的表名;
```

