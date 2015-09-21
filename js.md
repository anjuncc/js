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
Global
encodeURIComponent
eval
Math
--------
6.1.1 attribute 数据属性，访问器属性
Object.defineProperty(xx,"perperty",{configurable:false,value:'ff',writable:false,enumerable:false,get:fxxx,set:fxx})
Object.getOwnPropertyDescriptor()
6.2创建对象
6.2.1工厂模式
function createPerson(name,age,job){
  var o = new Object();
  o.name = name;
  o.age = age;
  o.job = job;
  o.sayName = function(){
    console.log(this.name)
  }
  return o;
}
var person1 = createPerson('anjun',29,"soft engineer")
6.2.2构造函数模式
function createPerson(name,age,job){
  this.name = name;
  this.age = age;
  this.job = job;
  this.sayName = function(){
    console.log(this.name)
  }
}
new createPerson(x,x,x) //只有用new调用才是构造函数
缺点 每个方法都在每个实例上创建一次
6.2.3原型模式
prototype 实例共享的属性和方法
function person(){}
Person.prototype.name = "f"
Person.prototype.constructor //Person
Object.getPrototypeOf()
6.2.4组合使用构造函数和原型模式
构造函数 定义实例属性 原型定义方法和共享属性
6.2.5动态原型
6.3继承 实现继承 不能接口味继承
6.3.1原型链
6.3.2借用构造函数
子类构造函数内调用超类构造函数
function SubType(){
  SuperType.call(this)
}
6.3.3组合继承
6.3.4原型式继承
