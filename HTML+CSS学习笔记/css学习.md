# css学习

### 1.什么是css

![image-20191120200040010](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191120200040010.png)

![image-20191120200124207](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191120200124207.png)

![image-20191120200145809](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191120200145809.png)

![image-20191120200211560](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191120200211560.png)

### 2.导入css的方式

1.内部样式表   *style标签*

2.链接外部样式  *link标签*

3.导入式  *style标签**@impotr url();* 

4.行内样式 ：*在标签内部添加style熟悉 style=“ color：red；...”*

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>2.css的导入方式</title>
    <!--内部样式表-->
    <style type="text/css">
        h1{
            color: #7e86ff;
            font-size: 30px;
        }
    </style>
    <!--链接外部样式-->
    <link rel="stylesheet" href="../resource/css/style.css" type="text/css">
    <!--导入式-->
    <style>
        /*@import url(../resource/css/style.css);*/
    </style>
</head>
<body>
    <!--行内样式-->
    <h1>hello,戴粤斌</h1>
    <h2>hello,css</h2>
    <h3 style="color: red;font-size: small">hello,vue</h3>
</body>

```



![image-20191120202457832](C:\Users\daiyu\AppData\Roaming\Typora\typora-user-images\image-20191120202457832.png)