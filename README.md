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

    getInfo('饥人谷', 2, '男');
    getInfo('小谷', 3);
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