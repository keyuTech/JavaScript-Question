# JavaScript-Question

## 一、JavaScript入门
1. 解释白屏和FOUC

2. 介绍一下repaint和reflow

3. 如何异步加载脚本

## 二、数据类型、运算符
1. 如何判断一个变量是否是数字、字符串、布尔、函数

2. 以下代码的输出结果是?
```
var a = 1;  
a+++a;  
typeof a+2;
```

## 三、运算符、流控制语句、函数
1. NaN是什么

2. break和continue的区别

3. switch case中的break的作用

4. 遍历数组，打印数组每一项的平方
```
var arr = [3, 4, 5]
```

5. 以下代码输出结果是什么？为什么
```
var a = 1, b = 2, c = 3;
var val = typeof a + b || c >0
console.log(val) 

var d = 5;
var data = d ==5 && console.log('bb')
console.log(data)

var data2 = d = 0 || console.log('haha')
console.log(data2)

var x = !!"Hello" + (!"world", !!"from here!!");
console.log(x)
```

6. 关于if(xx)和a==b的判断的区别

## 四、作用域、引用类型
1. 立即执行表达式是什么，有什么作用

2. 用递归实现n!

3. 以下代码输出什么？
```
function getInfo(name, age, sex){
    console.log('name:',name);
    console.log('age:', age);
    console.log('sex:', sex);
    console.log(arguments);
    arguments[0] = 'valley';
    console.log('name', name);
}

getInfo('A', 2, '男');
getInfo('B', 3);
getInfo('男');
```

4. 写一个函数，返回参数的平方和
```
function sumOfSquares(){
}
var result = sumOfSquares(2,3,4)
var result2 = sumOfSquares(1,3)
console.log(result)  //29
console.log(result2)  //10
```

5. 以下代码输出什么？为什么？
```
sayName('world');
sayAge(10);
function sayName(name){
    console.log('hello ', name);
}
var sayAge = function(age){
    console.log(age);
};
```

6. 以下代码输出什么？为什么？
```
var x = 10
bar() 
function foo() {
console.log(x)
}
function bar(){
var x = 30
foo()
}
```

7. 以下代码输出什么？为什么？
```
var x = 10;
bar() 
function bar(){
var x = 30;
function foo(){
    console.log(x) 
}
foo();
}	
```
8. 以下代码输出什么？为什么？
```
var a = 1
function fn1(){
function fn2(){
    console.log(a)
}
function fn3(){
    var a = 4
    fn2()
}
var a = 2
return fn3
}
var fn = fn1()
fn() //输出多少
```
9. 以下代码输出什么？为什么？
```
var a = 1
function fn1(){
function fn3(){
    var a = 4
    fn2()
}
var a = 2
return fn3
}
function fn2(){
console.log(a)
}
var fn = fn1()
fn() //输出多少
```

10. 以下代码输出什么？为什么？
```
var a = 1
function fn1(){

function fn3(){
    function fn2(){
    console.log(a)
    }
    fn2()
    var a = 4
}
var a = 2
return fn3
}
var fn = fn1()
fn() //输出多少
```

11. 以下代码输出什么？为什么？
```
var obj1 = {a:1, b:2};
var obj2 = {a:1, b:2};
console.log(obj1 == obj2);
console.log(obj1 = obj2);
console.log(obj1 == obj2);
```

12. 以下代码输出什么？为什么？
```
var a = 1
var c = { name: 'jirengu', age: 2 }

function f1(n){
++n
}
function f2(obj){
++obj.age
}

f1(a) 
f2(c) 
f1(c.age) 
console.log(a) 
console.log(c) 
```

13. 写一个深拷贝函数
## 五、JSON、Array
1. JSON 格式的数据需要遵循什么规则

2. 使用 JSON 对象实现一个简单的深拷贝函数(deepCopy)

3. 数组方法里push、pop、shift、unshift、join、splice分别是什么作用？用 splice函数分别实现push、pop、shift、unshift方法

4. 写一个函数，操作数组，数组中的每一项变为原来的平方，在原数组上操作
```
function squareArr(arr){
}
var arr = [2, 4, 6]
squareArr(arr)
console.log(arr) // [4, 16, 36]
```

5. 写一个函数，操作数组，返回一个新数组，新数组中只包含正数
```
function filterPositive(arr){
}
var arr = [3, -1,  2,  '饥人谷', true]
filterPositive(arr)
console.log(arr) //[3,  2]
```

## 六、ES5数组字符串、Date
1. 写一个函数，返回从min到max之间的 随机整数，包括min不包括max 

2. 写一个函数，生成一个长度为 n 的随机字符串，字符串字符的取值范围包括0到9，a到 z，A到Z
```
function getRandStr(len){
  //补全函数
}
var str = getRandStr(10); // 0a3iJiRZap
```
3. 写一个函数，生成一个随机 IP 地址，一个合法的 IP 地址为 0.0.0.0~255.255.255.255
```
function getRandIP(){
  //补全
}
var ip = getRandIP()
console.log(ip) // 10.234.121.45
```
4. 写一个函数，生成一个随机颜色字符串，合法的颜色为#000000~ #ffffff
```
function getRandColor(){
}
var color = getRandColor()
console.log(color)   // #3e2f1b
```
5. 实现一个flatten函数，将一个嵌套多层的数组 array（数组） (嵌套可以是任何层数)转换为只有一层的数组，数组中元素仅基本类型的元素或数组，不存在循环引用的情况
```
flatten([1, [2], [3, [[4]]]]) => [1, 2, 3, 4];
```
6. 实现一个reduce函数，作用和原生的reduce类似
```
var sum = reduce([1, 2, 3], function(memo, num){ return memo + num; }, 0); => 6
```
7. 写一个函数getChIntv，获取从当前时间到指定日期的间隔时间
```
var str = getChIntv("2017-02-08 10:30:24");
console.log(str);
```
8. 写一个函数，参数为时间对象毫秒数的字符串格式，返回值为字符串。假设参数为时间对象毫秒数t，根据t的时间分别返回如下字符串:
* 刚刚（ t 距当前时间不到1分钟时间间隔）
* 3分钟前 (t距当前时间大于等于1分钟，小于1小时)
* 8小时前 (t 距离当前时间大于等于1小时，小于24小时)
* 3天前 (t 距离当前时间大于等于24小时，小于30天)
* 2个月前 (t 距离当前时间大于等于30天小于12个月)
* 8年前 (t 距离当前时间大于等于12个月)
```
function friendlyDate(time){
}
var str = friendlyDate( '1484286699422' ) //  1分钟前
var str2 = friendlyDate('1483941245793') //4天前
```

## 七、正则表达式
1. \d，\w,\s,[a-zA-Z0-9],\b,.,*,+,?,x{3},^,$分别是什么?

2. 写一个函数trim(str)，去除字符串两边的空白字符

3. 写一个函数isEmail(str)，判断用户输入的是不是邮箱

4. 写一个函数isPhoneNum(str)，判断用户输入的是不是手机号

5. 写一个函数isValidUsername(str)，判断用户输入的是不是合法的用户名（长度6-20个字符，只能包括字母、数字、下划线）

6. 什么是贪婪模式和非贪婪模式

## 八、定时器、DOM
1. 下面这段代码输出结果是? 为什么?
```
var a = 1;
setTimeout(function(){
    a = 2;
    console.log(a);
}, 0);
var a ;
console.log(a);
a = 3;
console.log(a);
```

2. 下面这段代码输出结果是? 为什么?
```
var flag = true;
setTimeout(function(){
    flag = false;
},0)
while(flag){}
console.log(flag);
```
3. 实现一个节流函数

4. 简单解释单线程、任务队列的概念

5. 列出DOM 元素选取的 API

6. 如果创建元素、如何添加元素
