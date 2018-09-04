---
title: Markdown语法
date: 2018-09-03 17:05:10
tags:
---

基本语法
===

1.强调
---

星号与下划线都可以，单是斜体，双是粗体，符号可跨行，符号可加空格

**一个人来到田纳西**
__毫无疑问__

*我做的馅饼
是全天下*

_最好吃的_


2.分割线
---
三个或更多-，必须单独一行，可含空格

3.引用
---
符号后的空格可不要，内层符号前的空格必须要
> 引用
 >> 内部引用

4.标题
---
Setext方式
---
三个=-或更多

大标题
===
小标题
---

Atx方式
---
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

5.无序列表
---
符号之后的空格不能少，-+*效果一样，但不能混合使用，因混合是嵌套列表，内容可超长
- 无序列表
- 无序列表

* 无序列表
* 无序列表

6.有序列表
---
数字不能省略但可无序，点号之后的空格不能少
1. 有序列表
2. 有序列表
3. 有序列表
8. 有序列表

嵌套列表
---
-+*可循环使用，但符号之后的空格不能少，符号之前的空格也不能少
- 嵌套列表1
  + 嵌套列表2
  + 嵌套列表3
    - 嵌套列表4
    * 嵌套列表5
- 嵌套列表6

7.文字超链：Inline方式
---
Tooltips可省略
[helloztt](http://www.baidu.com "todo")

8.图片超链?
---
多个感叹号，Tooltips可省略，要设置大小只能借助HTML标记
!![GitHub Mark](http://github.global.ssl.fastly.net/images/modules/logos_page/GitHub-Mark.png)

9.索引超链：Reference方式?
---
索引，1 可以是任意字符
[不如][1]
[1]:http://bruce-sha.github.io

10.自动链接?
---
尖括号
<347871727@qq.com>

11.代码：行内代码
---
```java
class HelloZtt{
    public static void main(String[] args){
      System.out.println("On the Way");
    }
}
```


12.代码：段落代码
---
每行文字前加4个空格或者1个Tab
```
    System.out.println("On the Way");
    System.out.println("On the Way");
    System.out.println("On the Way");
```

13.注释
---
<!-- 注释 -->

14.转义字符
---
Markdown中的转义字符为\
\\ 反斜杠
\` 反引号
\* 星号
\_ 下划线
\{\} 大括号
\[\] 中括号
\(\) 小括号
\# 井号
\+ 加号
\- 减号
\. 英文句号
\! 感叹号

15.表格
---
项目     | 价格
-------- | ---
Computer | $1600

排版
===
1.段落缩进（空格）
---
半方大的空白&ensp;或&#8194;看，飞碟
全方大的空白&emsp;或&#8195;看，飞碟
不断行的空白格&nbsp;或&#160;看，飞碟
&emsp;&emsp;段落从此开始。

2.字体、字号、颜色
---
<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑</font>
<font face="STCAIYUN">我是华文彩云</font>
<font color=#0099ff size=12 face="黑体">黑体</font>
<font color=#00ffff size=3>null</font>
<font color=gray size=5>gray</font>

3.标签
---
快捷键 `Ctrl + D` 来收藏本页

流程图
===

* 将流程图代码包含在代码引用之间即可
* 流程图代码分两块，上面一块是创建你的流程（创建元素），然后隔一行，创建流程的走向(连接元素)
* 创建流程（元素）：tag=>type: content:>url
  * tag 是流程图中的标签，在第二段连接元素时会用到。名称可以任意，一般为流程的英文缩写和数字的组合。
  * type 用来确定标签的类型，=>后面表示类型。由于标签的名称可以任意指定，所以要依赖type来确定标签的类型
  * 标签有6种类型：start end operation subroutine condition inputoutput
  * content 是流程图文本框中的描述内容，: 后面表示内容，中英文均可。特别注意，冒号与文本之间一定要有个空格
  * url是一个连接，与框框中的文本相绑定，:>后面就是对应的 url 链接，点击文本时可以通过链接跳转到 url 指定页面
* 指向流程(连接元素)：标识（类别）->下一个标识
  * 使用 -> 来连接两个元素
  * 对于condition类型，有yes和no两个分支，如示例中的cond(yes)和cond(no)
  * 每个元素可以制定分支走向，默认向下，也可以用right指向右边，如示例中cond2(yes,right)。
  
```flow 
st=>start: 开始 
e=>end: 登录 
io1=>inputoutput: 输入用户名密码 
sub1=>subroutine: 数据库查询子类 
cond=>condition: 是否有此用户 
cond2=>condition: 密码是否正确 
op=>operation: 读入用户信息

st->io1->sub1->cond 
cond(yes,right)->cond2 
cond(no)->io1(right) 
cond2(yes,right)->op->e 
cond2(no)->io1 
```


---
参考资料：
1.[https://blog.csdn.net/qcx321/article/details/53780672](https://blog.csdn.net/qcx321/article/details/53780672)

