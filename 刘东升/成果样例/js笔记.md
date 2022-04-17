---
title: 3.20
date: 2022-03-20 15:40:01
tags:
---
# js笔记
## 1.输入输出代码
	alert(msg)浏览器弹出警示框alert('');
	console.log(msg)浏览器控制台打印输出信息
	prompt(info)浏览器弹出输入框，用户可以输入
## 2.用var设置变量名（剩下跟c++都相同）
	区别点：
	1.tm可以不声明直接用
## 3.进制
	8进制前面加0
	16进制前面加0x
	数字中的最大值Number.MAX_VALUE
	最小值同理min
	Infinity无穷大
	-无穷小
	NaN代表一个非数值
## isNAN
	用来判断非数字
## typeof
	判断数据类型
## 转换为string类型
加+''
## 转换为数字型
	parselnt(string)整数
	parseFloat(string)浮点数
## 逻辑中断
	&&前为真则返回后，前为假则返回前
	||前为真则返回前，前为假则返回后
	前面判断为假则不执行后面
## 数组创建
	1.利用new来创建数组
	例子：var 数组名 = new Array();注意A要大写
	2.利用数组字面量创建数组
	空数组var 数组名= [];	
	数组里的数据用,分隔
## 数组名.length可以统计数组长度
## 定义函数直接function
## arguments里面储存了所有传递过来的实参
## 可以函数表达式来命名
	var 变量名=function(){}
## 函数内部没有声明直接赋值的变量也属于全局变量
## 作用域练：内部函数访问外部函数的变量，采用的是链式查找的方式来决定那个值，这种结构我们称为作用域链
## 里面字面量创造对象
	例子：
	var 对象名 ={
		unname：'',
		age: ,
		sayhi: function(){
			balalala;
		}
		...
	}
## 利用new object创建对象
	var obj=new Object();
	赋值用=结尾用；
	输出方式还可以是：obj['sex']
## 构造函数，有点像结构体
	格式：
	function 构造函数名(){
		this.属性=值;
		this.方法 = fuction(){}
	}
	例子：
	fuction Star(uname,age,sex){
		this.name=uname;
		this.age=age;
		this.sex=sex;
	}
	new Star('刘德华',18,'男');
## for in遍历
	for(var k in obj)
	输出得到的是属性名
	obj[k]输出的属性值
## 文档查找：MDN/W3C