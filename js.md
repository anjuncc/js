html5 <script async 使用外部文件 不保证加载的顺序
一定在load之前执行
var num = -18
console.log(num.toString(2));//二进制
五种基本数据类型(undefind Null Boolean Number string)按值访问，参数全部是传值的，引用也是传值，不过表现了
出来就引用{
  function setName (obj) {
	obj.name = 'Nicholars';
	obj = new Object();
	obj.name = "greg"
}
var person = new Object();
setName(person);
rs  = person.name;
console.log(rs);//Nicholars
}
没有块级作用域
if for 等｛｝中定义的变量在全局作用域中
-----
{} = new Object()
a["fist name"] = 'ff' //访问属性方法
a.xx ='bb'//访问属性方法
Array() //可存不同任意类型
[] = new Array() =  Array()
shift unshift push pop reverse sort{比较 toString之后的值}
concat splice indexOf lastIndexOf every filter map forEach some reduce reduceRight
Date类型
RegExp类型
Function类型
函数名为指针 函数没有重载
函数声明与函数表达式基本一样
function f(){}  var f = function()
1 arguments.callee == f
2 this
3 f.caller 调用者
apply call 扩充函数运行的作用域,对象与作用域与方法耦合
window.color = 'red'
var o= {color:"blue"}
function sayColor(){
  console.log(this.color);
}
sayColor.call(this)
sayColor.call(o)
var objSaycolor = sayColor.bind(o)
objSaycolor()
