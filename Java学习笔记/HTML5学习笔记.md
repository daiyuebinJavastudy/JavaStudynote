# HTML5学习笔记

## 1.什么是HTML

HTML（Hyper Text Markup Language） 超文本标记语言

超文本：不限于文本，将其他媒体信息如图片，视频等通过超链接的呈现在网页的方式

标记：通过对文本的标记告知浏览器该如何显示文本的内容，这种标记方式叫做标签，分为单标签

```
<hr />,<br />,<input />,<img />,<meta>,<link>,<col>等
```

和双标签

```
<body>,<html>,<p>等
```

HTML它不是编程语言而是一种超文本标记语言，作用是描述网页的基本结构

![image-20191116192037472](img/image-20191116192037472-1573965525014.png)

快捷输入标签方法 例如p+tab键；

## 2.基本结构

```html
<!DOCTYPE html><!---指定文件类型为html-->
<html lang="en">
<head><!--头部-->
    <meta charset="UTF-8"><!--描述标签,指定字符编码utf-8-->
    <title>Title</title><!--标题-->
</head>
<body><!--主体，网页显示的内容-->

</body>
</html>
```

## 3.基本标签	

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>基本标签</title>
</head>
<body>
<!--标题标签-->
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<!--段落标签-->
<p>从明天起，做一个幸福的人</p>
<p>喂马，劈柴，周游世界</p>
<p>从明天起，关心粮食和蔬菜</p>
<p>我有一所房子，面朝大海，春暖花开</p>
<!--换行标签-->
从明天起，和每一个亲人通信 <br/>
告诉他们我的幸福 <br/>
那幸福的闪电告诉我的 <br/>
我将告诉每一个人 <br/>
给每一条河每一座山取一个温暖的名字 <br/>
<!--水平线标签-->
<hr/>
<!--粗体，斜体-->
<strong>粗体：keep studying</strong>
<br/>
<em>斜体：keep going</em>
<!--注释和特殊标签-->
空格便签：空&nbsp;格 空&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;格
<br/>
大于 &gt;
<br/>
小于 &lt;
<br/>
公司 &copy;感恩戴德
</body>
</html>
```

### 3.1图片标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>图片标签学习</title>
</head>
<body>
<!--绝对路径-->
<!--就是写死了的路径，例如：D:\idea\HTML\resource\img\1.jpg-->
<!--相对路径-->  
<!--相对于当前文件的路径，例如../resource/img/1.jpg-->   
<!--../指上级目录-->
<img src="../resource/img/1.jpg" alt="这是一张照片" title="这是一张动漫" width="400" height="400">
</body>
</html>
```

### 3.2链接标签

![image-20191117161629733](img/image-20191117161629733.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>超链接标签</title>
</head>
<body>
<!--超链接
1.target="_blank" 在新标签中打开
2.target="_self" 在原标签中打开
3.还有其他空格可选择
-->


<a name="top">顶部</a>
<a href="#bottom">回到底部</a>
<a href="https://github.com/daiyuebinJavastudy/JavaStudynote/blob/master/Java%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0/HTML5%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0.md" target="_blank">
    点击查看我的笔记</a>

<a href="我的第？个网页.html" target="_blank"></a>
<a href="https://baidu.com" target="_self">点击跳转百度</a>
<br/>
<br/><br/><br/><br/><br/><br/><br/>
<!--锚链接
<a  name="top"></a>
1.需要一个锚标记
2.跳转到该标记
-->
<a href="#top">回到顶部</a>
<a name="bottom">底部</a>

<!--功能型链接
1.邮件链接mailto
2.qq推广链接
-->
<a href="mailto:1006285232@qq.com">点击发送qq邮箱</a>
<a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=1006285232&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2:1006285232:53" alt="联系我" title="联系我"/></a>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>超链接标签</title>
</head>
<body>
<!--a标签
    target="_blank" 在新标签中打开
    target="_self" 在原标签中打开
-->


<a name="top">顶部</a>
<a href="#bottom">回到底部</a>
<a href="https://github.com/daiyuebinJavastudy/JavaStudynote/blob/master/Java%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0/HTML5%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0.md" target="_blank">
    点击查看我的笔记</a>

<a href="我的第？个网页.html" target="_blank"></a>
<a href="https://baidu.com" target="_self">点击跳转百度</a>
<br/>
<br/><br/><br/><br/><br/><br/><br/>
<!--锚标签
    <a  name="top"></a>
    需要一个锚标记
    跳转到该标记
-->
<a href="#top">回到顶部</a>
<a name="bottom">底部</a>
</body>
</html>
```

### 3.3行业元素 块元素

块元素：无论内容多少，都独占一行，开辟一块新的空间 (p,h1-h6)

行内元素：能够单独摆放在一行内的标签（strong, em, a）

### 3.4列表

列表就是信息资源的一种展示形式，它能把信息更加结构化，条理化的展现在我们面前，便于我们更加清楚的浏览信息

列表分为：

有序列表ol

无序列表ul

自定义列表dl

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>列表学习</title>
</head>
<body>
<!--有序列表
ol（order list）
-->
<ol>
    <li>java基础</li>
    <li>html+css+vue</li>
    <li>javaweb</li>
    <li>ssm</li>
</ol>
<hr/>
<!--无需列表
ul（unordered list）
-->
<ul>
    <li>java基础</li>
    <li>html+css+vue</li>
    <li>javaweb</li>
    <li>ssm</li>
</ul>
<!--自定义列表
dl：标签
dt：列表名称
dd：列表内容
-->
<hr/>
<dl>
    <dt>学习步骤</dt>
    <dd>java基础</dd>
    <dd>html+css+vue</dd>
    <dd>javaweb</dd>
    <dd>ssm</dd>
</dl>
</body>
</html>
```

### 3.5表格

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表格标签学习</title>
</head>
<body>
<!--表格标签
    table
    tr：行
    td：列
-->
<table border="1px">
    <tr>
    <!--colspan:跨列-->
        <td colspan="3" align="center">成绩</td>
    </tr>
    <tr>
        <!-- rowspan ：跨行      -->
        <td rowspan="2" align="center">daiyuebin</td>
        <td>英语</td>
        <td>120</td>
    </tr>
    <tr>
        <td>java</td>
        <td>130</td>
    </tr>
    <tr>
        <td rowspan="2" align="center">戴粤斌</td>
        <td>英语</td>
        <td>130</td>
    </tr>
    <tr>
        <td>java</td>
        <td>140</td>
    </tr>

</table>
</body>
</html>
```

### 3.6媒体标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>媒体标签</title>
</head>
<body>
<!--视频标签
    音频标签
    -->
<video src="../resource/Vedio/练习.MP4" controls height="400" width="400"></video>
<img src="../resource/img/love.JPG" alt="i'm in love with you" height="400" width="500">
<audio src="../resource/Audio/Kina - i'm in love with you.mp3" controls></audio>
</body>

```

### 3.7页面结构

![image-20191118194323207](img/image-20191118194323207.png)

一个页面的主要分为头部header，中间部分section，article，aside，nav，脚部footer

常用的三个header，nav，footer

### 3.8表单

表单的两种提交方式

get：可以在地址栏看到用户输入的信息，不安全

post：不能在地址栏看到输入信息

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表单</title>
</head>
<body>
<h1>注册</h1>
<form action="媒体元素.html" method="get">
<!--  value="默认值"：文本框默认值
      maxlength="8" ：输入的最大字符数
      size="30"：文本框长度  -->
    <p>用户<input type="text" name="username" value="admin" placeholder="请输入账号"></p>
    <p>密码<input type="password" name="pwd" value="1234" ></p>
    <p>
        <!-- 单选框
        type="radio"
        vaule:值
        name：组，name的值必须一样，否则和多选框没区别
        -->
        <input type="radio" value="boy" name="sex" disabled>男
        <input type="radio" value="gril" name="sex">女
    </p>

    <p>
    <!--   多选框
           type="checkbox"
         -->
        兴趣
        <input type="checkbox" value="code" name="hobby">敲代码
        <input type="checkbox" value="sport" name="hobby">运动
        <input type="checkbox" value="read" name="hobby">看书
        <input type="checkbox" value="music" name="hobby">听歌
    </p>

    <p>
    <!-- 按钮
        type="button": 普通按钮
        type="submit": 提交按钮
        type="reset" : 重置按钮
        -->
        <input type="button" value="点我">
        <input type="image" src="../resource/img/love.JPG" height="100" width="100">

    </p>
    <p>
        <!--下拉框,列表框-->
        想去国家列表
        <select name="想去国家选择" >
            <option value="china">中国</option>
            <option value="usa" selected>美国</option>
            <option value="EHC">瑞士</option>
            <option value="india">印度</option>
        </select>
    </p>

    <p>
        <!--文本域 -->
        <textarea name="textarea" cols="30" rows="10" required></textarea>
    </p>

    <p>
    <!--文本域-->
        <input type="file" name="files" >
    </p>

    <!--邮箱验证-->
    <p>
       邮箱验证 <input type="email" name="email" >
    </p>
    <!--url验证-->
        <p>
            url <input type="url" name="url">
        </p>
    <!-- 数字  -->
    <p>
        <input type="number" name="数字" max="10" min="0" step="1">
    </p>
     <!--滑块
     type="range"
     -->
    <p>
       音量<input type="range" name="number" max="100" min="0" step="1">
    </p>
    <!-- 搜索-->
       <p>
           搜索 <input type="search" name="search" id="mark">
       </p>
    <!--增强鼠标可用性
   -->
    <p>
        <label for="mark"> 点我试试</label>
        <input type="text" name="text">
    </p>

    <!--使用正则表达式的邮箱
        pattern=""-->
    <p>
        <input type="text" name="diy" pattern="/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/">
    </p>
    <p>
        <input type="submit" value="提交">
        <input type="reset" value="重置">
    </p>

</form>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表单</title>
</head>
<body>
<h1>注册</h1>
<form action="媒体元素.html" method="get">
<!--  value="默认值"：文本框默认值
      maxlength="8" ：输入的最大字符数
      size="30"：文本框长度  -->
    <p>用户<input type="text" name="username" value="admin" readonly></p>
    <p>密码<input type="password" name="pwd" value="1234" hidden></p>
    <p>
        <!-- 单选框
        type="radio"
        vaule:值
        name：组，name的值必须一样，否则和多选框没区别
        -->
        <input type="radio" value="boy" name="sex" disabled>男
        <input type="radio" value="gril" name="sex">女
    </p>

    <p>
    <!--   多选框
           type="checkbox"
         -->
        兴趣
        <input type="checkbox" value="code" name="hobby">敲代码
        <input type="checkbox" value="sport" name="hobby">运动
        <input type="checkbox" value="read" name="hobby">看书
        <input type="checkbox" value="music" name="hobby">听歌
    </p>

    <p>
    <!-- 按钮
        type="button": 普通按钮
        type="submit": 提交按钮
        type="reset" : 重置按钮
        -->
        <input type="button" value="点我">
        <input type="image" src="../resource/img/love.JPG" height="100" width="100">

    </p>
    <p>
        <!--下拉框,列表框-->
        想去国家列表
        <select name="想去国家选择" >
            <option value="china">中国</option>
            <option value="usa" selected>美国</option>
            <option value="EHC">瑞士</option>
            <option value="india">印度</option>
        </select>
    </p>

    <p>
        <!--文本域 -->
        <textarea name="textarea" cols="30" rows="10"></textarea>
    </p>

    <p>
    <!--文本域-->
        <input type="file" name="files">
    </p>

    <!--邮箱验证-->
    <p>
       邮箱验证 <input type="email" name="email">
    </p>
    <!--url验证-->
        <p>
            url <input type="url" name="url">
        </p>
    <!-- 数字  -->
    <p>
        <input type="number" name="数字" max="10" min="0" step="1">
    </p>
     <!--滑块
     type="range"
     -->
    <p>
       音量<input type="range" name="number" max="100" min="0" step="1">
    </p>
    <!-- 搜索-->
       <p>
           搜索 <input type="search" name="search" id="mark">
       </p>
    <!--增强鼠标可用性
   -->
    <p>
        <label for="mark"> 点我试试</label>
        <input type="text" name="text">
    </p>
    <p>
        <input type="submit" value="提交">
        <input type="reset" value="重置">
    </p>

</form>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表单</title>
</head>
<body>
<h1>注册</h1>
<form action="媒体元素.html" method="get">
<!--  value="默认值"：文本框默认值
      maxlength="8" ：输入的最大字符数
      size="30"：文本框长度  -->
    <p>用户<input type="text" name="username" ></p>
    <p>密码<input type="password" name="pwd"></p>
    <p>
        <!-- 单选框
        type="radio"
        vaule:值
        name：组，name的值必须一样，否则和多选框没区别
        -->
        <input type="radio" value="boy" name="sex">男
        <input type="radio" value="gril" name="sex">女
    </p>

    <p>
    <!--   多选框
           type="checkbox"
         -->
        兴趣
        <input type="checkbox" value="code" name="hobby">敲代码
        <input type="checkbox" value="sport" name="hobby">运动
        <input type="checkbox" value="read" name="hobby">看书
        <input type="checkbox" value="music" name="hobby">听歌
    </p>

    <p>
    <!-- 按钮
        type="button": 普通按钮
        type="submit": 提交按钮
        type="reset" : 重置按钮
        -->
        <input type="button" value="点我">
        <input type="image" src="../resource/img/love.JPG" height="100" width="100">

    </p>
    <p>
        <!--下拉框,列表框-->
        想去国家列表
        <select name="想去国家选择" >
            <option value="china">中国</option>
            <option value="usa" selected>美国</option>
            <option value="EHC">瑞士</option>
            <option value="india">印度</option>
        </select>
    </p>

    <p>
        <!--文本域 -->
        <textarea name="textarea" cols="30" rows="10"></textarea>
    </p>

    <p>
    <!--文本域-->
        <input type="file" name="files">
    </p>
    <p>
        <input type="submit" value="提交">
        <input type="reset" value="重置">
    </p>

</form>
</body>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表单</title>
</head>
<body>
<h1>注册</h1>
<form action="媒体元素.html" method="post">
<!--  value="默认值"：文本框默认值
      maxlength="8" ：输入的最大字符数
      size="30"：文本框长度  -->
    <p>用户<input type="text" name="username" ></p>
    <p>密码<input type="password" name="pwd"></p>
    <p>
        <!-- 单选框
        type="radio"
        vaule:值
        name：组，name的值必须一样，否则和多选框没区别
        -->
        <input type="radio" value="boy" name="sex">男
        <input type="radio" value="gril" name="sex">女
    </p>

    <p>
    <!--   多选框
           type="checkbox"
         -->
        兴趣
        <input type="checkbox" value="code" name="hobby">敲代码
        <input type="checkbox" value="sport" name="hobby">运动
        <input type="checkbox" value="read" name="hobby">看书
        <input type="checkbox" value="music" name="hobby">听歌
    </p>

    <p>
    <!-- 按钮
        type="button": 普通按钮
        type="submit": 提交按钮
        type="reset" : 重置按钮
        -->
        <input type="button" value="点我">

    </p>
    <p>
        <input type="submit" value="提交">
        <input type="reset" value="重置">
    </p>
</form>
</body>
</html>
```

进入用户登录网页，点击右键检查元素，Network，然后输入用户名密码提交，在检查栏点第一个网页然后点击header查看状态

![image-20191118200612422](img/image-20191118200612422.png)

表单元素格式

![image-20191118200742391](img/image-20191118200742391.png)

input标签里都必须要有name属性，他和你提交的东西是键值的形式存在，

![image-20191119200811025](img/image-20191119200811025.png)

![image-20191119202356736](img/image-20191119202356736.png)

### 3.9HTML总结

![image-20191119204241419](img/image-20191119204241419.png)

![image-20191119204249560](img/image-20191119204249560.png)